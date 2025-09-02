## `couchbase:enterprise-7.6.6`

```console
$ docker pull couchbase@sha256:d85a5bc76da69d75cfa473b9faefc1820cd67981c06ed2575516207092f6be50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.6` - linux; amd64

```console
$ docker pull couchbase@sha256:3fcddef6f647e2f8915bfea6ed4d88e47435be658f9eaf4c7023775265092ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.7 MB (794749781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0702dd8d062d42536620637cd452cd3467ccd8b0f69889d56fb2abbfbc64e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7881a498c80ade900eed4b3a2cabdd2fb78307ce4cba6f6a9b2f7299bda9765`  
		Last Modified: Tue, 02 Sep 2025 02:37:03 GMT  
		Size: 39.3 MB (39301277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d565aad6d0608bbe9fb0e80aea516949a3005f4a53b9eefc2582b92d8cf2c3`  
		Last Modified: Mon, 01 Sep 2025 23:44:23 GMT  
		Size: 926.6 KB (926584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670f5a3fe8d3c6c2da1fc46b66a9202d3ac07814ca858b820d4f342bb3db3504`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9199894c00e474e0f55bb5688b64ee0d325a8b23440ff36f7bcac7668cd54`  
		Last Modified: Tue, 02 Sep 2025 02:37:26 GMT  
		Size: 725.0 MB (724979808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6c9f796830d06dd0295393e7733d66d100a2bd9515596a3e04ce320f6fe834`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc724d557b7c7169d15cbc3b9a4098cd0a7a4bbf78b891664ef2b3b90fc54cb7`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0fe746b5de20ac95dcc35b5982666cdf6d2e46c4beef43f5699e95315db5b9`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61365f773e9ea027413c41b9b9e6131af7b5fdb4b8b404fe6049dc1f0675cae2`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ae58a42db7bf752bb061225927903b26a40eb57a952f1b0a190c19df2a451`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d31962623830b7bcf569d603bc17c817f7cda97e954f80b8e3e92a7e9612922`  
		Last Modified: Mon, 01 Sep 2025 23:09:55 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:6a34d290ea7cad31544b9aaf12a982a74e381fc186a64c819a144abee9519d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fd9df5324d0d5679ce19ee7600c87d0b03e4e690150a7f4c5db176d98b6d95`

```dockerfile
```

-	Layers:
	-	`sha256:d674a7a3c773472bebf0401a1581f27f18fe36ee9cf2055d5683659f76275bc9`  
		Last Modified: Tue, 02 Sep 2025 02:33:14 GMT  
		Size: 35.8 KB (35815 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:b904df00bf70c2e9b0035778fb7e8943b8d4c3d029ba6c0a036b05d5eb32e7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763423273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f134ee7e010a2ed456188b6e8f8c192d5867d4ed02fc52b96ef94a6774d5a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c65f527039e21f4424c92063f431ab9e3507ab759cac9415e5cd2200a7bce95`  
		Last Modified: Tue, 02 Sep 2025 00:25:43 GMT  
		Size: 38.9 MB (38858825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f68783af8e20cddabbc49a0fcaf7a010ef097fdbc925322c87727ee0057331b`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 772.2 KB (772178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd96e5d97dcd59426a79060dafbd0ae8a027ea59e9b937b330dd9dc4388b8fe5`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778311a1a08cd5c5587f6f55223bf4def9dcdbb040108e2b020742678cd5eabf`  
		Last Modified: Tue, 02 Sep 2025 01:22:48 GMT  
		Size: 696.4 MB (696425621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82e493bf57501314b1666388114456f7a011741f2c4d986cd41c3b7634d18a`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d99625602fc93fde009c14c612ba12abf06a0e628cacff4670d7995078a49`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef9dff6e792f54b727aa27f7f429c33991cc19fc6a387d73cdfb8a94fefc16`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6521aecd9cca8e29b467b8b25428e2d6601483cc5070693a7fa6be5e65ae8d8b`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b109feb514174a021f0479871d89c172d38c7f860397931de29b83cec67d1c62`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7e29904d3957640429a27d4cacb6ce6db43d7916f79df897fddbd33e5c8b25`  
		Last Modified: Tue, 02 Sep 2025 00:25:38 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:89409fb780726018c591e52558bcf9b5e89e8497f1b2a2c05f44167c73fec60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fae3f4025050a8b36fd2ed48486548e9281250fdaba12c3bce5e0bb8bb2722`

```dockerfile
```

-	Layers:
	-	`sha256:3a2a52656b8561207ca27485bf03aa6428f8fbd81b9973265910be214d10c260`  
		Last Modified: Tue, 02 Sep 2025 02:33:17 GMT  
		Size: 36.0 KB (36001 bytes)  
		MIME: application/vnd.in-toto+json
