## `couchbase:latest`

```console
$ docker pull couchbase@sha256:5df7918ac292d042a3102b71daf74b9ab1267407496c7213f214845ac6505937
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:9cd73917df2947a61c8dfb5475792f6260b5239b518e0d1d9ee06935b6a83b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **799.2 MB (799241553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc6e45a390861171a703ef60cb9052c89a267b0a52d97e0df03af2dab877b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Aug 2025 18:24:10 GMT
ARG RELEASE
# Wed, 13 Aug 2025 18:24:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 18:24:10 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 13 Aug 2025 18:24:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 13 Aug 2025 18:24:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=8baaddc8bedc7223db7995514996d87388b23fe6f39fecac7008ee8800be64f7            ;;          'amd64')            CB_SHA256=7bd09a72ec12c4dde2b78cf5354db814b58a9723ba3ba95b370d5d2320807a94            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["couchbase-server"]
# Wed, 13 Aug 2025 18:24:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 13 Aug 2025 18:24:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a3ee3f21170a6fcb9256f0ed54fdc5084b97e99ad459401ca795a3dd9c2061`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 43.8 MB (43806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3047574c10a774d6e419b5d133f12560b6c0c22a70bc6e223069d485c5d31b`  
		Last Modified: Mon, 01 Sep 2025 23:09:58 GMT  
		Size: 877.7 KB (877703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ee2cadc81e49c2dd8694407292e64f311cc6a3d24f9c4544f0efec2bdcfa4e`  
		Last Modified: Mon, 01 Sep 2025 23:09:57 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6770e2cc153b4313b16de10a031099c23677058cbfc4916881ebe26f1f2e6fd0`  
		Last Modified: Tue, 02 Sep 2025 02:35:43 GMT  
		Size: 724.8 MB (724827692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665e12387ccd3d579d2feac905a9c24c65530ab22d9bea1dd01d6005bb9d0da7`  
		Last Modified: Mon, 01 Sep 2025 23:09:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052ac385316703bca03dfb708fe37a4cc305330f4a3d2382ae38a42768e4b754`  
		Last Modified: Mon, 01 Sep 2025 23:09:57 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88508fbdf1166b31fda2e6df5524047f2d5b151422620a94439031c42ffcf8`  
		Last Modified: Mon, 01 Sep 2025 23:09:57 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2006956a4536380baf1e989859d0f4ac0233dece841cdf49e6bea138bfcd259a`  
		Last Modified: Mon, 01 Sep 2025 23:09:57 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32725626c6bf5ae331851c394e7fc58bd9409e679134b1c580bac035aeabc7cb`  
		Last Modified: Mon, 01 Sep 2025 23:09:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8664117eb693886d5e79c003b7c42cca2550bbc69a85e35130b849d556d736cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:58 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:38996b805432af832796d00722f5bd757368370080c10fcc6bbbc44bc60b487f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f58e80fedbed61d2b9a103d5f70f2272adb90dbce7d0a265c1389bdc36446`

```dockerfile
```

-	Layers:
	-	`sha256:29b2d3857e736cf15bd090fd308e84cb1e4880e392e6f37630170c6c787de003`  
		Last Modified: Tue, 02 Sep 2025 02:33:22 GMT  
		Size: 38.2 KB (38181 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:65deea4a95a2d322e46b2bf989c367daea2c5315ec85d94b24e42cad34a87539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.5 MB (769538021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b87f571a1e7643d6baefe486b3ae441bb44e50381c9106d6a65624029da7df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Aug 2025 18:24:10 GMT
ARG RELEASE
# Wed, 13 Aug 2025 18:24:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 18:24:10 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 13 Aug 2025 18:24:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 13 Aug 2025 18:24:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=8baaddc8bedc7223db7995514996d87388b23fe6f39fecac7008ee8800be64f7            ;;          'amd64')            CB_SHA256=7bd09a72ec12c4dde2b78cf5354db814b58a9723ba3ba95b370d5d2320807a94            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["couchbase-server"]
# Wed, 13 Aug 2025 18:24:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 13 Aug 2025 18:24:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb29f6fa4dd895fb5dc341dd162defe28e02d9fef43fbfd3255c4558725d8fa`  
		Last Modified: Tue, 02 Sep 2025 02:36:48 GMT  
		Size: 43.6 MB (43624132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473bddc4e227b512da258537be6d5ee8eb31ca70500fc56f7402d3ab5db1e2e7`  
		Last Modified: Tue, 02 Sep 2025 00:47:16 GMT  
		Size: 764.7 KB (764654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526d43d7bef6f348a377e28fe6a403d35924b89c0453b9dcad185fd593b4832f`  
		Last Modified: Tue, 02 Sep 2025 01:05:37 GMT  
		Size: 3.7 KB (3728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbd4cda9aedccf941f60afa4ff1e0cb234c374d2910ff1b37aca8e4fc110c37`  
		Last Modified: Tue, 02 Sep 2025 02:38:09 GMT  
		Size: 696.3 MB (696281997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b07046b74a48fb1578155a045dfcf5f029bce00f8fb83e2ebfc0879c2774df7`  
		Last Modified: Tue, 02 Sep 2025 01:05:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dddf5211b5010aa9015029cf0c1686fbc293c3285191b080f0e564bf34406b`  
		Last Modified: Tue, 02 Sep 2025 01:05:37 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a93a2dbda4f453e5ae599546698d0b423c4ff8df8ac4c90db268817773d766`  
		Last Modified: Tue, 02 Sep 2025 01:05:37 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0792a748d30ea522a2729addd4b91f1547c654eb8cdc290c6a6a6f34fca7857e`  
		Last Modified: Tue, 02 Sep 2025 01:05:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56d4162ee68bb45cac5db977eb962429912a3b8225e60bb5cce8b9cbdc9fbf1`  
		Last Modified: Tue, 02 Sep 2025 01:05:37 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b59cdc083fbeb3cae24c35b9c55878f7cb81e85a73bc9e2c135ccd461c4e6a`  
		Last Modified: Tue, 02 Sep 2025 01:05:37 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:eba72329a5d707fed55ca39d7c0bede8cda6a7e0ff4d19c1465fe487bd533793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 KB (38390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64bbfd9f41af8491cc67e6aba034cd19cd7f924f544c08e0b720fed9924a491`

```dockerfile
```

-	Layers:
	-	`sha256:dc4879ac46f6e3c139ab0b7e7b94b1529f4dd54cc367337742012d28040f5bde`  
		Last Modified: Tue, 02 Sep 2025 02:33:25 GMT  
		Size: 38.4 KB (38390 bytes)  
		MIME: application/vnd.in-toto+json
