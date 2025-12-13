## `couchbase:enterprise-7.6.1`

```console
$ docker pull couchbase@sha256:caf84ff04d8472d28fa82020e06dfd7f9a91ace0628e093be46ff790cac40a0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:a288b99ddfb16be04f97e535fcc02ea5d15576646a4af4ccddd0f04d71d682de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.8 MB (759839442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a72b26963dc1e8803a312b576a7569ab961cc45be0f70b5575f7d93fa1b887`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:15:18 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:15:18 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:15:18 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:15:18 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:15:45 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 13 Nov 2025 23:15:45 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:15:45 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:15:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:16:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:16:51 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:16:51 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:16:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb8ee256dfa604178aba0a3b17d5e03c5646169a401b6d6287d557340e98c16`  
		Last Modified: Thu, 13 Nov 2025 23:18:05 GMT  
		Size: 39.3 MB (39298745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac4cd9bf0139cd5915ab376519f078a1ee2306e3e3dc0934043b03a61baf168`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 926.7 KB (926739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc7dd1ffe0a637e047fb392dce92043f24857d250a9763ccb58c159b6f4652`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad40ece256362e3bb1bda9e797bbbd4db14fc688c9b86d43ace402e32045542e`  
		Last Modified: Fri, 14 Nov 2025 00:32:07 GMT  
		Size: 690.1 MB (690071979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e7252d410d2e5ce7ee00923147623b562f446ab5e8ed4734175e35feda20a`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94af77fb068f265641ce77333d4e972874c374992c096c566d6ece27d247cf6`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dee9cc8ec03d3f56c38531fd531711910bec9048088c7d85d99836ce476eb9`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b27aa682346727327a47652cace97d25cb8bd9975089e0c762723c8307fc7e`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972ae19cb22482d1e1aa130efa1036b5cc7a2bdb5a1c5454c0f5dea20ed34301`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1328b3797570c7801691be274de5b1e2b57480883e072233ed48afdf5c96718a`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:8146d0473bf634bb47020efcd85925ffb193077e99331dcf56f89871057330ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fb27c9d505028560b32566f950da8c5ed318764f32ac320e539ad54eeb4594`

```dockerfile
```

-	Layers:
	-	`sha256:cb6dfbaae75d456d0870d6951f5da18b45fdacd74b1f2c690dc69966fe559ee5`  
		Last Modified: Fri, 14 Nov 2025 00:31:43 GMT  
		Size: 37.5 KB (37521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:a9e0aa8eabdb16ed27933a72e8241971d8f000a030e7e8761e9d0a9772dee883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.0 MB (731954512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c7afaab4b3986beb5eaffeb95ecf239d2de2bb463c43f962c3d0ccbef67ed4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:15:26 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:15:26 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:15:26 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:15:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:15:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:15:50 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 13 Nov 2025 23:15:50 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:15:50 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:15:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:15:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 13 Nov 2025 23:16:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:16:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:16:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:16:54 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:16:54 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:16:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb3692e9c12a41663f9f38cb7f5c722830fa8077ebbb5f6bd9112afa2a16133`  
		Last Modified: Thu, 13 Nov 2025 23:18:13 GMT  
		Size: 38.9 MB (38872598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163c52cc087ec818c2c8d2ff7453c918247dff98814105b220c11d85d8c5e0f2`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 775.3 KB (775312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efbe36f73de891047be07418313af0d70784db9a97cd733ba0cf5e78daf46c`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c71a9a41b5a212bf128c7180173680a13ffd921a02c1d916a522795981a4df4`  
		Last Modified: Fri, 14 Nov 2025 03:33:24 GMT  
		Size: 664.9 MB (664917539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd07bf64d26c39f07f266dc23f016494ffc5c0876ead7b65db10633c06fd7f5`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fc1f4f044b4c8ff087e709e1fdc8391784b73c7bad7599a0be5878fe13db90`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65b097eec88c841514ae794d7a07350ae1d5d1ce14c0ff414f454deb378c3e5`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212eee7a037bef63f38963f6d375606cabbf23c625d515652d434699696c267d`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004c0e7d6063b0d521e14f89ad5ca6025af4e1b264c48587833aef79b179bb5c`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bae3600323a756a2074e457b4b3fbcb07b3743a8937512a89875d5a73f4a11`  
		Last Modified: Thu, 13 Nov 2025 23:18:10 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:d5105b9fbc217b35d93c9b51528df733bc386425d1a5cc8be589f5aa4b7c4177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26310dc0ebd202997f1f9163dea76b08cef90226ae12e9876c70ef8a5b2f8a1`

```dockerfile
```

-	Layers:
	-	`sha256:8430dbcc92fad851230b3fce408272940c8e41fe67fc325fd72cc02bddc5cd70`  
		Last Modified: Fri, 14 Nov 2025 03:32:45 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json
