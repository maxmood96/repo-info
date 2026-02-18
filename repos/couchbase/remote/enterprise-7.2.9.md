## `couchbase:enterprise-7.2.9`

```console
$ docker pull couchbase@sha256:446e718c62f9d8c0439d6dd7d5b322b032bc44de9aee8dc7a3a62d941f7a5151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.9` - linux; amd64

```console
$ docker pull couchbase@sha256:36c69ae0ff3e3e17e6fce1486db1e17e9e6aea1555a6757539938d059401135b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.9 MB (713882586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da746e6992c199e0a15219470b576edaca13b999ebe5c2761a105cc774f01f53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:49 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:12:49 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:12:49 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:12:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:13:22 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:13:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9
# Tue, 17 Feb 2026 20:13:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:13:22 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:13:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1f894b910a15d727c7f7d1c2daa3b3e0d4107dc4d6aff5f353aa501006875e31            ;;          'amd64')            CB_SHA256=af822187cd62b562b54d46df3f8b1161a1e7ee753ebf9a22e3da2d74ddf644f8            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:15:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:15:41 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:15:41 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:15:41 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ec6c78beeb1b72849f8bc2625638ae7e1ce84d8c5d258666bec3fa73c745d9`  
		Last Modified: Tue, 17 Feb 2026 20:14:55 GMT  
		Size: 43.8 MB (43815718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60edb222a760fe8646c44f5ec6db5fb8c8eae88bd5cfe847fcc20a73eb0ed03c`  
		Last Modified: Tue, 17 Feb 2026 20:14:52 GMT  
		Size: 2.0 MB (1995273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1b9668c38cd249d8d4e78c8980e507a362a83e7f7fc07b8bc712c16db9635`  
		Last Modified: Tue, 17 Feb 2026 20:16:31 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee37da1843cb87da35a183e6639f0dabf3764ca02038c403c022ae60a0c57b`  
		Last Modified: Tue, 17 Feb 2026 20:16:43 GMT  
		Size: 638.3 MB (638337003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf8fc2985cf54fe0dc55e47db29e230790ef87aade35013d6484dac1457a0c`  
		Last Modified: Tue, 17 Feb 2026 20:16:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff97c6b9ae3a28ff79d22a93da039f189c09cdb4d7ae967462a5570393730d9b`  
		Last Modified: Tue, 17 Feb 2026 20:16:31 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3eca627a7b52b9dcc16d99ee4b78b1b25ab06934c94338db0184f4736d3683`  
		Last Modified: Tue, 17 Feb 2026 20:16:32 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2152325f677d3b300635c0b3ba803d73589e1f68181e971db57c44bda1e3959`  
		Last Modified: Tue, 17 Feb 2026 20:16:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7a9982d61bda67de607053239b2abe7dc6fe82ea02ff3bc64bf736a19223c6`  
		Last Modified: Tue, 17 Feb 2026 20:16:33 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf5f4da331ea0899dc28d3bcb66113f374281b58e6ac5e221859081c0914b97`  
		Last Modified: Tue, 17 Feb 2026 20:16:34 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.9` - unknown; unknown

```console
$ docker pull couchbase@sha256:1b076b365c958d45bf4b30644ea0598ae1b4a7b01fbe82149e619eefc480d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ec29d744a851a3b0ea1cb69c8caaab627728925edc003f77eb24f73d1ae36e`

```dockerfile
```

-	Layers:
	-	`sha256:857741c42a7a95980df49687844dd9377c28a0cd0fb80b5aecc95e7f846c2999`  
		Last Modified: Tue, 17 Feb 2026 20:16:31 GMT  
		Size: 37.5 KB (37532 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.9` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:5bb0b670eed4e26b1140f619940b3e0bf63d71d5a2ead3cb850c6f601b89b44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.0 MB (686961854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfd1546d61f5ee5367b698d523ae7b0ec945b2d7478521a49bd5b8d5748bb91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:45 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:12:45 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:12:45 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:12:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:13:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:13:14 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9
# Tue, 17 Feb 2026 20:13:14 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:13:14 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:13:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:15:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1f894b910a15d727c7f7d1c2daa3b3e0d4107dc4d6aff5f353aa501006875e31            ;;          'amd64')            CB_SHA256=af822187cd62b562b54d46df3f8b1161a1e7ee753ebf9a22e3da2d74ddf644f8            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:15:33 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:15:33 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:15:33 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:15:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e761161c428d14659014745077a593df9cc10387fe5487f26afd3c86015b6cde`  
		Last Modified: Tue, 17 Feb 2026 20:14:43 GMT  
		Size: 43.6 MB (43630527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4695d34c70d30bdaad96c6c982510186afbb6453d9080c6abbcf5d62d02ba91`  
		Last Modified: Tue, 17 Feb 2026 20:14:41 GMT  
		Size: 1.8 MB (1832559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb44699c685a997c6690d15f4f9eee0c1e28819be4d4994f265c12bf37d5892`  
		Last Modified: Tue, 17 Feb 2026 20:16:15 GMT  
		Size: 3.7 KB (3727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6739dd21dd6b01de3bce26ffa19a4b666663c3263ff8a9258b3b7dccd5493c`  
		Last Modified: Tue, 17 Feb 2026 20:16:26 GMT  
		Size: 612.6 MB (612626660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef20ea62388f852b0d8d890fd6784ef6e1cfeebb6adcbd9739fee4eeb4b2ac64`  
		Last Modified: Tue, 17 Feb 2026 20:16:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619615734e65767e97a04a329286eab0d6f9e1e4e937d0af31a23aaafb66e14b`  
		Last Modified: Tue, 17 Feb 2026 20:16:15 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966968cb5b55bae1d0330fc85d31c161f567cb984a1e5d1c6c8ec1d809fd1a14`  
		Last Modified: Tue, 17 Feb 2026 20:16:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba093e2ba0ca57fcbf0e13a9482954c200a16e49d01a7b7b58110829f42d1d`  
		Last Modified: Tue, 17 Feb 2026 20:16:16 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287ca81ccccb1e6d54c10385f4d225efacc2b3f2f190a89ec86b9a9928d7b61d`  
		Last Modified: Tue, 17 Feb 2026 20:16:16 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ffbe1f1f1cd27aec908f4d9e07455c7e4fcfffea353fe38610cf1de99e300`  
		Last Modified: Tue, 17 Feb 2026 20:16:17 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.9` - unknown; unknown

```console
$ docker pull couchbase@sha256:e5dcc4e8b9812d29aa2df552a7f8f8b80b54f07bb3b4fbe24d67c6b50bdcdc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3fcf7a05eab6f9acd6c87f8cd3f8a32079840853fc75dab62b201db2c5116b`

```dockerfile
```

-	Layers:
	-	`sha256:0d700172fefadda0e82de41bbca2d882d11704be7f89c1fc8ba5bfe210b7abd7`  
		Last Modified: Tue, 17 Feb 2026 20:16:15 GMT  
		Size: 37.7 KB (37717 bytes)  
		MIME: application/vnd.in-toto+json
