## `couchbase:community-7.6.2`

```console
$ docker pull couchbase@sha256:61b39e2175626f582af7013c2b50cadea7a9901b1345d56bb8db061ae7900b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:3b6fa5f952a842bd0183385837690db99dc61dca9105ebc4651444e71d6dee94
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398391184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d397db0aef913d4e9ba34c10518e7a5495ed26d3ce1d11fbd5b11cfc3ddde9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:22:12 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 02:22:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 16 Oct 2024 02:22:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:22:28 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 16 Oct 2024 02:22:55 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 16 Oct 2024 02:22:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Wed, 16 Oct 2024 02:22:55 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Wed, 16 Oct 2024 02:22:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 16 Oct 2024 02:22:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 02:22:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 02:23:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:23:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 02:23:52 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 02:23:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 16 Oct 2024 02:23:53 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 02:23:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 02:23:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 16 Oct 2024 02:23:54 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 16 Oct 2024 02:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 02:23:54 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 02:23:54 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 16 Oct 2024 02:23:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a75f1093d68c4a4df16d8da90c0a7fa5de10d215bc15c4dfb921639b3da9d`  
		Last Modified: Wed, 16 Oct 2024 02:32:33 GMT  
		Size: 6.2 MB (6204670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b2d185509813a24f9505cb9d5a616a84d04580eaea45ae3f2e4d2afdf5757`  
		Last Modified: Wed, 16 Oct 2024 02:32:32 GMT  
		Size: 1.1 MB (1092446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35393ffce76c81f577c35143142d52f929a43b8fb03997b81ab018086ce262a6`  
		Last Modified: Wed, 16 Oct 2024 02:32:32 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a940f4d849f3964d8d634f511d908d331a58ef2f6f926212b0dfb750ccd28f1`  
		Last Modified: Wed, 16 Oct 2024 02:33:14 GMT  
		Size: 362.5 MB (362505113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b0ea6f5f48f160e1011eef1fbe5adf6c382cfb49eb213fbacc8cfe6a114892`  
		Last Modified: Wed, 16 Oct 2024 02:32:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c698cf9cd3586df60e5a4e671f4c427ba54ca0aafe34644884ec83ff047782c9`  
		Last Modified: Wed, 16 Oct 2024 02:32:30 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4205065b9172a2a1142311c1d492ef3b6a2b546e12cd128076029cb37176bbec`  
		Last Modified: Wed, 16 Oct 2024 02:32:30 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb8bbcaf2873135372ef6b9aa042b6abbd07a4f0b08f377c0fb5a01dbda5f9a`  
		Last Modified: Wed, 16 Oct 2024 02:32:30 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684b5df59980a05b83418320bb55623ed6c1e00361ee03300d74a11fc9fd538a`  
		Last Modified: Wed, 16 Oct 2024 02:32:30 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bc1325ff83964abe359bae3f5035d1633762fcdf20d290cf91a1ed949bd085`  
		Last Modified: Wed, 16 Oct 2024 02:32:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6bac9255f4b84462f3ed04426344275962de5de5c98d6c2a14fe8b2a7a0499b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.0 MB (375954683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3852fbaac8fe004e9af36c78d973e0eab6d71ef871ecee9b4cdf90b7fbe46f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 00:58:37 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 00:58:38 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 16 Oct 2024 00:58:38 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 00:59:12 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 16 Oct 2024 01:00:25 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 16 Oct 2024 01:00:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Wed, 16 Oct 2024 01:00:25 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Wed, 16 Oct 2024 01:00:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 16 Oct 2024 01:00:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 01:00:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 01:01:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 01:01:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 01:01:13 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 01:01:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 16 Oct 2024 01:01:13 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 01:01:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 01:01:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 16 Oct 2024 01:01:14 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 16 Oct 2024 01:01:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 01:01:14 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 01:01:14 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 16 Oct 2024 01:01:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78e6f6941d8212e81ac25e018b1ead37c0c44c9ed155d6f48148bda886de531`  
		Last Modified: Wed, 16 Oct 2024 01:06:15 GMT  
		Size: 6.0 MB (6041871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc7c114f093f2a5b8b90e9f681ab5cbe80a551963e43c9758c3323999f692b6`  
		Last Modified: Wed, 16 Oct 2024 01:06:13 GMT  
		Size: 938.0 KB (938015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1165e9d8ab0bb25afb2df11e27036b0c49116a52c9653fd6f25f1b2a4890e971`  
		Last Modified: Wed, 16 Oct 2024 01:06:13 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5dc141ee0abf780f7daf2e8b066b9b89bbec88d09389a6841a379894be3b4`  
		Last Modified: Wed, 16 Oct 2024 01:06:44 GMT  
		Size: 341.8 MB (341765530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36e1aa3f24418df9198f9ed017fbf1494730f4340cafb2d45276c182eb878f4`  
		Last Modified: Wed, 16 Oct 2024 01:06:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9322c57daa64f366b526844735ecbb026dd6985c77c82c067ed52d5f774ff7`  
		Last Modified: Wed, 16 Oct 2024 01:06:11 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597c8a459753238d0a9c277b463d42252d742b3833d96bdf5b94dc4dcdc5f1c2`  
		Last Modified: Wed, 16 Oct 2024 01:06:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcfb85fc4042040ad8c8084a08609a578b1694ef5269e90019a4aeb8d7afc5e`  
		Last Modified: Wed, 16 Oct 2024 01:06:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c630a3f5c41e1bb991e8405a210fab4289de638f2b6e3d1cca15620b1b63b40b`  
		Last Modified: Wed, 16 Oct 2024 01:06:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a27b362928d7d0d4842e1d5bb004ac330a91fd33c52ef01c4c2463ac93657a5`  
		Last Modified: Wed, 16 Oct 2024 01:06:11 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
