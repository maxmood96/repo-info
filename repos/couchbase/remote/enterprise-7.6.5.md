## `couchbase:enterprise-7.6.5`

```console
$ docker pull couchbase@sha256:0822fa288b15a3e0d38a2d142ad4a2e45002f6b98db4b3a693b821aeefda83ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:1b3f3e470173b64a1630fbd299026377dcd2e25131e682b22a7d1fc9e7fef6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771505172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0904c9ed4e46f7885682499328a821cf6e91f42fe94f4709a341f4b7a915a44e`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dae68379338e82a2bcc69be2a4667340444b828f878f05259ccd17af1b7e2a`  
		Last Modified: Thu, 02 Oct 2025 04:58:59 GMT  
		Size: 39.3 MB (39302310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31dd116c5ef62b0426c4d88c260387eeb32225e342204c2d057eee471bb8f15`  
		Last Modified: Thu, 02 Oct 2025 04:58:57 GMT  
		Size: 926.6 KB (926647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c19f0d18f5a2f18393f7545d0a57768ae0ee62834bfd2dd67fb9760da93e`  
		Last Modified: Thu, 02 Oct 2025 04:58:57 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4b1e69f200cff2e938b239bdcb44691bd9ca05b8de498200f0cf82dc4a84d5`  
		Last Modified: Thu, 02 Oct 2025 05:35:23 GMT  
		Size: 701.7 MB (701734222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464d11cdea705d0a2d31b623649d41d111ce32142a97fb17cdbf12d6b7f453a4`  
		Last Modified: Thu, 02 Oct 2025 04:58:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc85e372ceb34b432ecf3af95f7759edc2389083d2cdebfcb822ba0b3920d19`  
		Last Modified: Thu, 02 Oct 2025 04:58:57 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8faf7e202041152d68faac3fbac12fabe51df6c0d3d23c47de1d5afe7334229`  
		Last Modified: Thu, 02 Oct 2025 04:58:57 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bffa5e6f71a6f73e8fb085aac123a9a46fa8b70e443434756c7eab0fceee745`  
		Last Modified: Thu, 02 Oct 2025 04:58:59 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e747793ae4e4d31de12ceb909f8c3c1b687ff176572350bbe300482192dcb0`  
		Last Modified: Thu, 02 Oct 2025 04:58:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9db669a619a27559ba5485b31860b9db254a65d3e29996ea2a1c6b354f3313f`  
		Last Modified: Thu, 02 Oct 2025 04:58:57 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:12aad10f6922d7a81f0cb4a53d517ba706294df1507328c6b78204dbfba82ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a7150aa3365c1cd407797ddc2cb5518cbb9dc6091aef00423024adac64666d`

```dockerfile
```

-	Layers:
	-	`sha256:5b1d1cb606a131374b2cd3592d3740349299f60b71460ff4384b4a9b19a05df6`  
		Last Modified: Thu, 02 Oct 2025 05:32:30 GMT  
		Size: 35.8 KB (35815 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:49c7a5c451744d1b6256b9aa21b36e49e35870627d048050a436b4d8e3f436ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742487544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a58bc8543973661112c92cbef790f7d7f5ccdb1acc191a6d676bbdf2d8429cf`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee556f46b2c8d05a9357dad788ee843a705c85fc28c0c1541f8d22e5cf2002e2`  
		Last Modified: Thu, 02 Oct 2025 01:15:01 GMT  
		Size: 38.9 MB (38858081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d53930346b6f7f65cb04aa58854ce77ec27e1ea996e6abfc6b10a6ec4de504`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 775.2 KB (775218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db805c83614cc31ecde7a99de41feacd9e0875737cfedda295a7615de9baa354`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdee1c6f26d3b3972536cc9d5434214d82072fe6cd786bb1e45c110ee99da0`  
		Last Modified: Thu, 02 Oct 2025 02:27:45 GMT  
		Size: 675.5 MB (675465963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd51abb3dddb7d4a0e6de47c56f1aee062a751c9bb7641461078f647803c162`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643e3df291a8ab00e1cf90de862c9cbaf09649853d697610aba77e83b5c2a6fc`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bae07b60701d958de0a555a9fdbe1c238a52a1bed0be82d56a35ebc5bae5e7`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1385a3576fbb0d0f7c145fc35151ea200aa606450f48beb4d7bfd61abfeced1a`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59091be5e01bc64a25c8b550d0ac7449c096b92b85b8317b9e9d0647212b56a`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4007f6d0a9b8ce2f793b8323a99365e7cb53587e98bc6f74db6bd3bec6da95c`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:f531b8bb2ba3802683f3494f3f97f0f618fe0db0e9512425e2ad2fc6aee2682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a2719ab1d6e3439eabfcf32b11cb4c059a66727af447650e886f492d01b77d`

```dockerfile
```

-	Layers:
	-	`sha256:9a5d4e9027b01e590430b72a32be2b1883fccfccd352386351d406dcf342979c`  
		Last Modified: Thu, 02 Oct 2025 02:31:59 GMT  
		Size: 36.0 KB (36001 bytes)  
		MIME: application/vnd.in-toto+json
