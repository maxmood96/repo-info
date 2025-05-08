## `couchbase:enterprise-7.6.5`

```console
$ docker pull couchbase@sha256:7320a44562cfd8a505ab7f961dc5dc28e93b53d4dad2cfcfe183631e460d6119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:8ac7c15ba4cc0f30f59af48aa9650ac97d370d2f52621b03eb13ecd3062ef9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771502888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e187dd6f714996ff0b63253a8a7fa4c45bcaf068cf79561d0dd31da96c1c56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a4d6db8a190ebe2395546f3972edabbc9b1952b75d6e661f3c3b2b8f5dc038`  
		Last Modified: Thu, 08 May 2025 17:12:06 GMT  
		Size: 39.3 MB (39303030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aced536e5608cc9b4e944bf63d75746183bbf6796c33f91617a28dbbe8cb2b81`  
		Last Modified: Thu, 08 May 2025 17:12:06 GMT  
		Size: 926.8 KB (926781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cd23edae327e9bde7f94d779fdd7d5b12c48ecdac799b71fdf6fa99137981`  
		Last Modified: Thu, 08 May 2025 17:12:06 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87f570f249d3f1947e28090b590249a5128d0b1c5d1ac59bff6bf5d3761e16f`  
		Last Modified: Thu, 08 May 2025 17:35:16 GMT  
		Size: 701.7 MB (701735287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3e4039b4bdb44a80d5db68a00f65809e51cc9f0cafc654a42e250916102bea`  
		Last Modified: Thu, 08 May 2025 17:12:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c53477008e0f12877a42873b0815858374c667ab74add561d208b2613bc87`  
		Last Modified: Thu, 08 May 2025 17:12:07 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c844a01f71b5cccc1dfbfbeeacffe5fa7d6a1ae7590649719130ba6e3c0072b2`  
		Last Modified: Thu, 08 May 2025 17:12:07 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53610df5341d5faecbf1ce270eb06917e9adc2135969ce8ce58d5e1470eb9923`  
		Last Modified: Thu, 08 May 2025 17:12:07 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0c8a11f6118b8d91789fd495b9592488e10ef26542435c8407ccda06fc260`  
		Last Modified: Thu, 08 May 2025 17:12:07 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55af96468facbb8d4dc9081cff55d6068ac60aa4002fec7258c8b3b76257e8d`  
		Last Modified: Thu, 08 May 2025 17:12:08 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:ae28ba2c866a13c238666e0ef839a85eaefb7274d47de679b20a440079b61205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cd1d313b358536ef7f05122573b0820ef376d0a930a1c0d6373cb99714a5dc`

```dockerfile
```

-	Layers:
	-	`sha256:7bcdb4c6e75f8068fc5dfbaf1fbdd7a2940b70b86ef56412bb22a9c5719d8b99`  
		Last Modified: Mon, 05 May 2025 16:36:38 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9ad1848bbb498c96c029397d2037963e7de4f9276f886e536d16b22e391943ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742445470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b54f3e91eee1096a711578aef64b15e3cffd68e20e784a15d7b4701b555550d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b69c28fa1ad00449b43e2dcc461469d322baf59409f913b4659f56ae06b8230`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 38.8 MB (38849198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f84499f3538d7f520e660577d11d5fa60aa5061e42e15d98d29c4b1fd891e3`  
		Last Modified: Thu, 08 May 2025 17:05:18 GMT  
		Size: 770.7 KB (770748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab1e0c02d38a83ff152b4a6ff3b32650cd5283e3d9c84baaceca17105bc1b8`  
		Last Modified: Thu, 08 May 2025 17:05:20 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f908b82d63933d99148cf2c031bff1da5d972a7b19e4be8bb9c1108f4bb85a`  
		Last Modified: Thu, 08 May 2025 17:16:33 GMT  
		Size: 675.5 MB (675466131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d259b259d11a255500910b199793d507306bd47f78599b0b8ea2adce3ad0ea`  
		Last Modified: Thu, 08 May 2025 17:05:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aacdfb5024bd5bcbcf80dfa37d492e346b5282842216094871225acf042db20`  
		Last Modified: Thu, 08 May 2025 17:05:22 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77491c91436026d786a4e868078396e532536722206f633579d9a1a26c470e6`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5465916d8d071d4ce0314c8caf7cd7cf07db3c6f128c64e2c3314d86fae1b7`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d7914eb7dd45413ef221828e83fd62a9968979a0bee40bfea32140acfd37f`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd6cfb15c80190b9b53b7b523e9891a6a7e216afd2499ec968f836f7cd5f883`  
		Last Modified: Thu, 08 May 2025 17:05:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:9174e8c685ecd6a564187ca37aea3c5d007ac76702ac8d51902f1990470ee303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837add3a724ea8c75fba139cfe8899bd00f308d1988b2ba569d954230331f602`

```dockerfile
```

-	Layers:
	-	`sha256:91403b41563b18c1e9be94fd6562572cd75a21c2e1f728a49fdc54332712d3c3`  
		Last Modified: Mon, 05 May 2025 16:43:14 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json
