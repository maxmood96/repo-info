## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:912e320a6715f4d074412d369590b34455fa8c115f6391e6219e0190392dc5c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:847fd2fb71a5a5c3405933ac125971990980e76f94918c153e4ae73085ea6ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **799.9 MB (799921699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5d1ee119d7803570a80a5342fb7a8b10d180d8c6f5e64ae432d22d96546b85`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184795cc07acdef84c2198f0544e8f9054d7c2a6cb24c00d1749d64e151e4ebb`  
		Last Modified: Thu, 09 Oct 2025 22:20:57 GMT  
		Size: 44.5 MB (44485932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b109192a7cbde9cf774bc45aff89c775e6f3763cdf1a4e30915dfb0a1f93924`  
		Last Modified: Thu, 09 Oct 2025 22:02:35 GMT  
		Size: 878.0 KB (878050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64680a9587c7e49cd9b5039cfcf2aab85c0ed0ec5abe4834ba71b534f4ee3e66`  
		Last Modified: Thu, 09 Oct 2025 22:02:35 GMT  
		Size: 3.7 KB (3722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81c55fd16a2d92879463cc082b5b3e1c2f926b9a80a044013206d77eecd37d`  
		Last Modified: Thu, 09 Oct 2025 22:21:43 GMT  
		Size: 724.8 MB (724827587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395fc4658fdec66f16057e0b1ec40fc543778c05dc4a6cc331969b18d8bff374`  
		Last Modified: Thu, 09 Oct 2025 22:02:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29aa8b8699a670cf9ceafdb10f6c002d5916e5e7593acd59e1c46238442370d7`  
		Last Modified: Thu, 09 Oct 2025 22:02:34 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60c2f5cd1d1dc54e65dece1b0274befe71d794a2c922915c5bd87890888bde9`  
		Last Modified: Thu, 09 Oct 2025 22:02:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9989bdf01cdfb4e3b5e2bbe380a9bcb7809a89d387421bcc9383638109c947d`  
		Last Modified: Thu, 09 Oct 2025 22:02:35 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f84ff9dccc2c24e23e28b065a352a7e8765edc2325bd7c845f5b3138634967a`  
		Last Modified: Thu, 09 Oct 2025 22:02:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770bd3ac486b1310050dcb8f2fbac39961c2de27170fe0acf0e14cc8786dcccf`  
		Last Modified: Thu, 09 Oct 2025 22:02:34 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:d5dc748b6c0dbe83aef965b4d1670e375da89dbeea2fa4d7c3106ac7887794df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418f8e68e242177caa5b14762a4d18bcfe8a06cc2e224e8961cfedfce8c1d9d`

```dockerfile
```

-	Layers:
	-	`sha256:6bf5f13fb4f77d6c3544581dce3f025576ab18a03481a43a0bda51cdc6959f8c`  
		Last Modified: Thu, 09 Oct 2025 23:35:29 GMT  
		Size: 38.2 KB (38180 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:41d165e6f8e882906125deffaf921c7906b2ed1c891cc29ee6cfb96b94c52a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.2 MB (770218893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9187a593ab37ebf8c03c66b906835948179b6fce9e686e95a8f97505d8557501`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897b230dff5435754d4a588ca493e3ac6025e644459dc4f8da12479121a9f823`  
		Last Modified: Thu, 09 Oct 2025 22:20:43 GMT  
		Size: 44.3 MB (44302545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3972e6b381bdfa80b995bb82a4ec1ea499f1893c843142a19567e86089c060`  
		Last Modified: Thu, 09 Oct 2025 22:02:37 GMT  
		Size: 765.2 KB (765161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83c7d26c6a045f911052b8e85b336a4f1ee93c60f4d5309b241f22f04f95047`  
		Last Modified: Thu, 09 Oct 2025 22:02:38 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caabafc0c1827561b1210eab4e6df3eba280aa5d43156d56c889f6782cb442bf`  
		Last Modified: Thu, 09 Oct 2025 23:36:01 GMT  
		Size: 696.3 MB (696282486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c67f341d30e575f47f7d88cfc1693803f6bd81f764efedc49610cc2f529a6a`  
		Last Modified: Thu, 09 Oct 2025 22:02:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8166f5e1223bd2b74800b0378c4d61c3e3c1930356a8c098bbc489ed45797f`  
		Last Modified: Thu, 09 Oct 2025 22:02:38 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9026624bca29cc0019b0f8e86f4ac48fba618c7ba59284ec164aa49bdca07c`  
		Last Modified: Thu, 09 Oct 2025 22:02:39 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c03606fa8d5294216a14966a00cff9fcdc3526405259b9caabad01d1c4b51ff`  
		Last Modified: Thu, 09 Oct 2025 22:02:39 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b54e9059c69cdb3f5e9f52d7120daf6548d19a5fd2ce944fe999d1a7a3f27`  
		Last Modified: Thu, 09 Oct 2025 22:02:39 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518c91a94f0775599963440ab15a0807349a36414eea01c30b6866937aff999`  
		Last Modified: Thu, 09 Oct 2025 22:02:38 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:65cceb5fde1f029df11714165ec9462affa63de8dd4a3d389dc43c4a51483b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 KB (38390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52f210af56f0252f3235a8435879c85f6c9bb0b06d707332249b96d96009684`

```dockerfile
```

-	Layers:
	-	`sha256:20c99755af3adfe89127cebfd8b3a6c3568b5ca35d9b9c83721355e8b103a2b4`  
		Last Modified: Thu, 09 Oct 2025 23:35:32 GMT  
		Size: 38.4 KB (38390 bytes)  
		MIME: application/vnd.in-toto+json
