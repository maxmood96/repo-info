## `couchbase:enterprise-7.6.6`

```console
$ docker pull couchbase@sha256:e28ce1f3b0986099b80f0527ff186f3c1287a76dc1ea64e590d2aa264b0f687b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.6` - linux; amd64

```console
$ docker pull couchbase@sha256:61b078503d182c029dfe826b5ba79f26d737612d8ebc6294d7e30f1d4ff3d289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.9 MB (795878696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f159ac86def1c6eb9cd6a34e84da17bb39b62c6ab620f2e7dc9396974ea85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:16:45 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Mar 2026 01:16:45 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Mar 2026 01:16:45 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Mar 2026 01:16:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Mar 2026 01:17:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Mar 2026 01:17:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 17 Mar 2026 01:17:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 17 Mar 2026 01:17:15 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Mar 2026 01:17:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Mar 2026 01:17:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:18:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:18:07 GMT
CMD ["couchbase-server"]
# Tue, 17 Mar 2026 01:18:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Mar 2026 01:18:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0001bcf2a16ddd96b52a216ecafc544a5101ccc013c63cd08e52e856cbfc3a6`  
		Last Modified: Tue, 17 Mar 2026 01:19:00 GMT  
		Size: 39.3 MB (39302615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1ed2b96ebda4034c56e45ce88529ffcc3dd5358747a052a4818044721d9b9`  
		Last Modified: Tue, 17 Mar 2026 01:18:58 GMT  
		Size: 2.1 MB (2052281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0c1bd4390c043c0bb0f6520f50a76123d60f66dd9f2645444556333c0330c`  
		Last Modified: Tue, 17 Mar 2026 01:18:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13d95185957fd9d988b91c98ccc882214f708db4866aafd121a26ca2e909e4a`  
		Last Modified: Tue, 17 Mar 2026 01:19:15 GMT  
		Size: 725.0 MB (724980101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf94a1fe2fbeb125fc7eab800e74dd2eef6b4d2bf8fdd0c72291c3605c0cb3f`  
		Last Modified: Tue, 17 Mar 2026 01:18:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc71a8f9f15f182b1d6a163ba0fb1bf7836cc92fef1cfed64b785f11d1713ab8`  
		Last Modified: Tue, 17 Mar 2026 01:18:59 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1031578e10f9d21b660342a6cbb4544f523b056433e36596dbba9df157b5fe44`  
		Last Modified: Tue, 17 Mar 2026 01:19:00 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d479e7f02999feacdd4f26318ef17277aa9cf955f686d12c9cc9a1fbaedd4c7`  
		Last Modified: Tue, 17 Mar 2026 01:19:01 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4dd9155bf3b17551b188bf8eb137666de09e01fbcab851fee7b196d6ef8601`  
		Last Modified: Tue, 17 Mar 2026 01:19:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8533213a1f0e8deae501be0af4f05b783637cea498006fea5a88958e6ff5af2`  
		Last Modified: Tue, 17 Mar 2026 01:19:02 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:47972d5b6cdcdac59198f137099f4cf8d2f7b94b777017f555c24c2ea272ff9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b28bf1506117f44b4dc9fb89e83f37eb49b6f8559d0c394cc6114ba16a5b25`

```dockerfile
```

-	Layers:
	-	`sha256:66636b50b46c096fd7dae6ebf53f4a0a548452dda062d8e98c19ac4b0e56d895`  
		Last Modified: Tue, 17 Mar 2026 01:18:57 GMT  
		Size: 35.8 KB (35783 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:fd6ef0fb0f30e9ca6bd6ba69d83780987526cf63431d19f6ea968facbf0557e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.5 MB (764545596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872291bb61030b85954cca3a847196391fab7e351432a102dea12a9f5ce3bb49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:16:52 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Mar 2026 01:16:52 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Mar 2026 01:16:52 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Mar 2026 01:16:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Mar 2026 01:17:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Mar 2026 01:17:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 17 Mar 2026 01:17:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 17 Mar 2026 01:17:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Mar 2026 01:17:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Mar 2026 01:17:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:18:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:18:19 GMT
CMD ["couchbase-server"]
# Tue, 17 Mar 2026 01:18:19 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Mar 2026 01:18:19 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9679c475fab5ffaa5006207a25e6b6a3eb5bcda204c3bb4fe00b03102422aa4`  
		Last Modified: Tue, 17 Mar 2026 01:19:11 GMT  
		Size: 38.9 MB (38865464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4182904545e39a235773fce5bb7bcc763314485d856bc33adf5d0a5d3f4c7f3`  
		Last Modified: Tue, 17 Mar 2026 01:19:09 GMT  
		Size: 1.9 MB (1858485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783ef06158efc63d70201e319a52821044a7bde255e7611a2a13c4e5e5ff27f9`  
		Last Modified: Tue, 17 Mar 2026 01:19:09 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e36e0840d7e1f54407bed0b7fad955fc37bc8429e052b836dc37c4b4d439f76`  
		Last Modified: Tue, 17 Mar 2026 01:19:22 GMT  
		Size: 696.4 MB (696427448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8c260c54e1df75c1c94e1b1b83081410fe5d80266058ab54b3ea1fd657e493`  
		Last Modified: Tue, 17 Mar 2026 01:19:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a222c143533271c58b0ea07f7befd60fbcd5db3c84c9c98d37b42b4e7f896e41`  
		Last Modified: Tue, 17 Mar 2026 01:19:11 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48b80e416ebe93d1add3cedb306d1273f0671276ae48a2844674aac822f131d`  
		Last Modified: Tue, 17 Mar 2026 01:19:12 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fb982b7f7b66ab3c83611437efa9d344a86466e1c65fde1aa836a10ec5fe47`  
		Last Modified: Tue, 17 Mar 2026 01:19:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a1758ab70f70c8e8b9007092794a793b36779c6c6a169eb372a5aac7167424`  
		Last Modified: Tue, 17 Mar 2026 01:19:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb433ad03d5dc86abefab4f5c94653a5ff745471ab5d8583526fb5f583044229`  
		Last Modified: Tue, 17 Mar 2026 01:19:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:4e1d6b2e07c2d9a6483b7f00b4121f6e5acb799ee516fbe9f258ba8f998da863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27594033da7c0aa74fe4874c937ec9c73f128846f3341347d037d917138a0f5`

```dockerfile
```

-	Layers:
	-	`sha256:edbe7eec791cf728f410d71e3148ded01ff671bc9123ef967f3347526334188e`  
		Last Modified: Tue, 17 Mar 2026 01:19:09 GMT  
		Size: 36.0 KB (35968 bytes)  
		MIME: application/vnd.in-toto+json
