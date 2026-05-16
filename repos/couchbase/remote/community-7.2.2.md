## `couchbase:community-7.2.2`

```console
$ docker pull couchbase@sha256:3d6e1e6799107ba693ff2e03dbb24af7aac2817d104a3f960b6c762bd7e34e99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:ee22d07d7e9f0b129c239a7946e74d71a729c0466bb6023a9ef562dd5d2b60f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 MB (396546597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f5913b9a9bbf8c85745a3281871c59f5b595024e60e0b90621476e6b8b43b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:11:44 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:11:44 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:11:44 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:11:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 15 May 2026 21:12:06 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:15:05 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:15:05 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:15:05 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:15:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:15:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:15:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:15:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:15:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:15:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:15:06 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:15:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:15:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311826ae161dd1a63f0ee5a8720b4fe1cb420e567d17dc86b9a60f290d67e4be`  
		Last Modified: Fri, 15 May 2026 21:14:07 GMT  
		Size: 39.3 MB (39307398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012944883d1bab8927bc4289e694be475ca0a77defa9a80ed0454c9f5275a18d`  
		Last Modified: Fri, 15 May 2026 21:14:05 GMT  
		Size: 926.8 KB (926789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb091be68df93c651e575dd2f685bbc0a18d7f28ebada984177f9795b41bd0`  
		Last Modified: Fri, 15 May 2026 21:15:41 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee092885b6d3beae3b92e50673dd2f5930a925803ab6abfef81a94ae2ccfe507`  
		Last Modified: Fri, 15 May 2026 21:15:48 GMT  
		Size: 326.6 MB (326570543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05eec84ed278f58dd36fb3c70e93d8068c82fbd136f0ba4806aed60d1f78f5`  
		Last Modified: Fri, 15 May 2026 21:15:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86286d1fc664d30a3a76f55e5988b66f313a117a75288a42f11836c70e22e115`  
		Last Modified: Fri, 15 May 2026 21:15:41 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4160b8808a46eb83d3891920732f40b64eda8f022337297640ee760425eacf4`  
		Last Modified: Fri, 15 May 2026 21:15:43 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287bb0a97f6ea6bf6825dcaa47fd30809c9405dad8d2971e536543f23037ba9`  
		Last Modified: Fri, 15 May 2026 21:15:43 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e1cecf0f0d480dbece469d930f679f4d8c718451cf7228a7b681ee42ea4be1`  
		Last Modified: Fri, 15 May 2026 21:15:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1a5da47acfe482a6578ad8a8ae6a66ec4d75e989a78ec00e3e6f48e8ec5e9`  
		Last Modified: Fri, 15 May 2026 21:15:44 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:bdfe09b0b77bc897116d3a85e106649618ed987d4c28e8bc664c95f22a1bc638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7fff081fa9ecde4f8d7012129cd2746599725dfccc1c0360bcdbed16b1d2d7`

```dockerfile
```

-	Layers:
	-	`sha256:9a8f85cb2583c05d41faf387294397bd87bae1219326dbe1c077c7b97b2c9d60`  
		Last Modified: Fri, 15 May 2026 21:15:41 GMT  
		Size: 37.2 KB (37207 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:302095d4ddbda851b57e56dea8e5f93641e0dd6fba9317fbc1a1e26ce9a93e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.0 MB (371991686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c73a6cc4947119e295b8ba90ffd75182c29d5bc26485facaa3cfe70b29f8445`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 15 May 2026 21:12:32 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:32 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:15:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:15:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:15:26 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:15:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:15:27 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:15:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:15:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:15:27 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:15:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:15:27 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:15:27 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:15:27 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7d30015a0862163891ad0be17003188ca0b88f67cc845fc95b96afe7cf75e9`  
		Last Modified: Fri, 15 May 2026 21:14:33 GMT  
		Size: 38.9 MB (38866692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6518710b9a0cb6f0348ed8ae58b1fc00d0941a5c3928aee6ac3b00d2fbe53`  
		Last Modified: Fri, 15 May 2026 21:14:31 GMT  
		Size: 775.3 KB (775259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2921c3da4ce5f4ffbd2b285ead0107183dff9dac0c4c1dd17c615d1805d36d`  
		Last Modified: Fri, 15 May 2026 21:15:57 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33380a57d908afe2cd3408fd39cf26e7751c6a037301f474d0641038c5172413`  
		Last Modified: Fri, 15 May 2026 21:16:05 GMT  
		Size: 304.7 MB (304737929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d810205d01d579d0708517eeff61a6e58a49df21f64dd7b785de1621cedeecaf`  
		Last Modified: Fri, 15 May 2026 21:15:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfeed72b46fcd05844ba3bf354c275aba75cb268cc79aeae7d6773adaebef7b`  
		Last Modified: Fri, 15 May 2026 21:15:57 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98afe689585eb87addf3315db4f1c23586602b580ca0a560ecb607321ca391fd`  
		Last Modified: Fri, 15 May 2026 21:15:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966371a74c52f632aa827f323cdd374f972c472eced371895552502c29b1dd3`  
		Last Modified: Fri, 15 May 2026 21:15:58 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1682f061947232a7bbc805d6db7ab6ca47947866c79c7bd677d414321bc3564`  
		Last Modified: Fri, 15 May 2026 21:15:58 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2a9b9d6958c21f895f53fa133776b126c7af98370cffda8e85c79342b7b2f2`  
		Last Modified: Fri, 15 May 2026 21:15:59 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:ecc222d99b04355529a1501143949b58b26afcd62d2a6b0cfd356fffa606d8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f30eb1c94e7f65f3c06eaada7dfc27a518b8748d5c049e23827884c08c7a6`

```dockerfile
```

-	Layers:
	-	`sha256:391de672dc32c4f34ee3e5153c422ced2f6d2699cde7d655625d8e458f081dc0`  
		Last Modified: Fri, 15 May 2026 21:15:57 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json
