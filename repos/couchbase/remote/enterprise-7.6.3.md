## `couchbase:enterprise-7.6.3`

```console
$ docker pull couchbase@sha256:5eced8c09d822cadb9d7aa11482fc6ebd0e788a88ac3d39f9e2d208902cef0ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:34b6f2d018f282779784d0f6ca6b2aefc7c87fe36829ab8f326dca7d40ab91da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 MB (768955155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b95faceec68d25ed9989fd2d027a8ae5459754771ef975e96eb880d4c9ef0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:39 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:13:39 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:13:39 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:13:39 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:14:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:14:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Tue, 17 Feb 2026 20:14:07 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:14:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:14:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:14:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Feb 2026 20:14:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:14:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:14:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:14:57 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:14:57 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:14:57 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5484155dee93d48d4a996515d91a4e71aebb280feedf2885a53c1b04fa584ea`  
		Last Modified: Tue, 17 Feb 2026 20:15:49 GMT  
		Size: 39.3 MB (39303119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81d5a9614849522ebc2ba78e8acff7de47c6c10db59287ab95c1a7caf2dcf87`  
		Last Modified: Tue, 17 Feb 2026 20:15:47 GMT  
		Size: 926.8 KB (926757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10acafd5caeb5d9a602d8d71147406abd0050db997897a56cb38a00e70988bc8`  
		Last Modified: Tue, 17 Feb 2026 20:15:47 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c289d9eb681fcf24c04d0d345a602df5bf3dc9de6812bcc8c2a72124b09abfec`  
		Last Modified: Tue, 17 Feb 2026 20:16:01 GMT  
		Size: 699.2 MB (699182728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c43d10e8be379d072e6b62abf76f5283a1959ce67adc772e1b0065ef1e5b4f8`  
		Last Modified: Tue, 17 Feb 2026 20:15:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e5de768cf4a8bb09656dd1dbac098209487a7912c66c2d7959450da635d3b8`  
		Last Modified: Tue, 17 Feb 2026 20:15:49 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4600dfd670f44e0bb4c7b3e42dbf799cfb86a29cd38edd8e50df7ec4ae46c7`  
		Last Modified: Tue, 17 Feb 2026 20:15:50 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b133874fa84a3fa2bf0e7693f4c3e6aa46aa46e0671e803961eed0f2c19dd90e`  
		Last Modified: Tue, 17 Feb 2026 20:15:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b36fd14f1d3788121507a8eccf4230feb228b650d0e4459d59cdaa400a9004`  
		Last Modified: Tue, 17 Feb 2026 20:15:51 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e0b71b8016768a4d9269bce2fceddd3279877174cdd4420e600c7743d42eef`  
		Last Modified: Tue, 17 Feb 2026 20:15:51 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:cf60b1f7477e06523bdf2d23bbb0a31d490860352a5c4101e76c865dc512d0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce0bf0ec616d15dd8d62a02d84daeec1124e8231c3a405ea7fdbb72087d3825`

```dockerfile
```

-	Layers:
	-	`sha256:af731028395cfbaa091b24c61fcdef3a4ce920b436bc919798cc2b8f835ac013`  
		Last Modified: Tue, 17 Feb 2026 20:15:47 GMT  
		Size: 35.8 KB (35773 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:41f25e44c72d8d1adab69295e476112f6ecf6ce484e97cfc96f458e0c2d2dddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.3 MB (740328124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e512129152effbb5f37bbfc22ab948ada434b8b151ee6a893acd7e1f8e0a72`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:55 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:12:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:12:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:12:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:13:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:13:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Tue, 17 Feb 2026 20:13:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:13:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:13:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:13:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:14:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:14:31 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:14:31 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:14:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f18b151d8d7222c7f76a84481a28495bfcd3f93b7ff85377aecb481adb7173`  
		Last Modified: Tue, 17 Feb 2026 20:15:24 GMT  
		Size: 38.9 MB (38867544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f007d9f8c372a6a2cc7a565f93190533c500a34e077221a44447a1edb693750`  
		Last Modified: Tue, 17 Feb 2026 20:15:22 GMT  
		Size: 775.3 KB (775329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeffb9472a509a49f93d774a7a32e9ce68bef8953929b04a2d53b542c208b79`  
		Last Modified: Tue, 17 Feb 2026 20:15:23 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5b9fb9a70af13227a366ee0bcc24b40cd5fe2363ff6ce553d421877b1bcffe`  
		Last Modified: Tue, 17 Feb 2026 20:15:35 GMT  
		Size: 673.3 MB (673295132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dcea32f411f7875119520dc2e4686b7cd83aa8eb3ba505a94c06a95ea7552`  
		Last Modified: Tue, 17 Feb 2026 20:15:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d8944845c00965905f177e02c50fe4919f40d9f0aa25beea73f1a1f99107fd`  
		Last Modified: Tue, 17 Feb 2026 20:15:24 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0f9a0893fbaba768e1a7ada8a571c99df9756629412715c6dacde38555a257`  
		Last Modified: Tue, 17 Feb 2026 20:15:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b69076beb1b88b9ae494f0528fe6f34ee0d7a7df62baf4a20eab7174b417f`  
		Last Modified: Tue, 17 Feb 2026 20:15:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babea51733d396a951114b18913ba6cb1f7e07bad8300412c8bc08d75b47db45`  
		Last Modified: Tue, 17 Feb 2026 20:15:26 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e895c6476b3e01a80bbe2ab82e9fd027a684f7ace9addc2217c59dc8771950b1`  
		Last Modified: Tue, 17 Feb 2026 20:15:26 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:71ce1742d7c768619f26eeed9ae19b79b8775ba642b6f165bba7673d017c6f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8946890c37b42945bd0d0cbc900f8218389e38804cebfd41f08cd8062c2432e6`

```dockerfile
```

-	Layers:
	-	`sha256:d2c24285a2cf3751bd1b6aaf20eba3c552893df5f48c4f13cd498f2f190d6bf8`  
		Last Modified: Tue, 17 Feb 2026 20:15:22 GMT  
		Size: 36.0 KB (35958 bytes)  
		MIME: application/vnd.in-toto+json
