<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:7.0.5`](#couchbase705)
-	[`couchbase:7.1.6`](#couchbase716)
-	[`couchbase:7.2.6`](#couchbase726)
-	[`couchbase:7.6.4`](#couchbase764)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:community-7.1.1`](#couchbasecommunity-711)
-	[`couchbase:community-7.2.4`](#couchbasecommunity-724)
-	[`couchbase:community-7.6.2`](#couchbasecommunity-762)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-7.0.5`](#couchbaseenterprise-705)
-	[`couchbase:enterprise-7.1.6`](#couchbaseenterprise-716)
-	[`couchbase:enterprise-7.2.6`](#couchbaseenterprise-726)
-	[`couchbase:enterprise-7.6.4`](#couchbaseenterprise-764)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:7.0.5`

```console
$ docker pull couchbase@sha256:60c8ccd24f777fe39ff9efc279d2be4d06d3b16a25d44ea9ba6c0953758e6607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchbase:7.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:60e2a7c09d0ff030dc539ca343adabf08a5f82a68dd6116615ba4ae3c953dea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.4 MB (615421160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026745745bfc815225fc02520deb37c093b0bd428e52391c582783e3eed27025`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1ca44819ce1f6620cdda7080ff7d0d00ab67bdd4d617046725fb60c37a0a`  
		Last Modified: Tue, 12 Nov 2024 00:57:56 GMT  
		Size: 6.3 MB (6299140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da62334b6d5935e1d2a21e75d4a90660d2a6ce9feaa3e4f8c308d92e2997c5a`  
		Last Modified: Tue, 12 Nov 2024 00:57:55 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2812246da48a667f0f533a58a1d53d9329d02316879be4bbbe44d28e3aeb333d`  
		Last Modified: Tue, 12 Nov 2024 00:58:08 GMT  
		Size: 581.6 MB (581606645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f12568e81669c3486dfefd3a7ec4251a7502beaef457d25b6cd8073431ed8`  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1ef0f44e68c300f1b04ffda254e09257c2150fcbbf5cbe979646878a86d57`  
		Last Modified: Tue, 12 Nov 2024 00:57:56 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731368a59d5ffc85e090fbf063db28fa568ba90bf829199413abc0e88931d79`  
		Last Modified: Tue, 12 Nov 2024 00:57:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cba7f2fc85eb14a8ef77fbbb3efa0e7b64132f2856e22b3c5e2351884c502f4`  
		Last Modified: Tue, 12 Nov 2024 00:57:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3a70bf740ffde435aad8b4f4ec9f9418c4ef0b1610fb10dfe7e952f6c8062`  
		Last Modified: Tue, 12 Nov 2024 00:57:57 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4415972b5950cb7d95b8c95a3cd363dd571eb483d08ed7b481c7558b8619d84d`  
		Last Modified: Tue, 12 Nov 2024 00:57:57 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.0.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:407c6dc9a9899fdf806edcc66b01ebd5b970d34a24e09049f5d459ef98113b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866f35aa2740a6df461d16c3bd389b4e16fc77aa94b97d21362f67396d7c477e`

```dockerfile
```

-	Layers:
	-	`sha256:452aaa5b1049883bfb1688c7f984bd35b27bac79e7da69c10357ea1c8de38e7c`  
		Last Modified: Tue, 12 Nov 2024 00:57:55 GMT  
		Size: 31.0 KB (31010 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.1.6`

```console
$ docker pull couchbase@sha256:caaffdc32520e19d03e313cf8f54db669d66a4dcc305d01c47d7f07fcb013485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:f6fbfea040c78f888b1b371de3af6c2ab9d7a3e61802a191ea49cdae564621eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650734358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d966266515710c09ca1890e71d9b6b0d607ba26c42a75cb7a82ba286fe02b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8afbf2f1c19b5c3d3c4cbe897177ce3c9840d161fc0565a3c6efab784eb292f`  
		Size: 6.3 MB (6299173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400bc3fbd7c94e788acf49bf00e316d1fcd9b182010d90c30381eae089bc06bb`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c89ce562297e58a96cd81b8b1fe5443d7b6ff2b214d58811cada4e2e83db8`  
		Last Modified: Tue, 12 Nov 2024 00:58:22 GMT  
		Size: 616.9 MB (616919823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae46418d8da2075f00a6844dabd34032253c4a34143808208e0077ea08f6b96d`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c4ca65edb4e0fa9d1ca9147de9136660a5418572cb221bfdcf3e59a1750e8f`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8eccd799a40e46d685be5d2f321899fbc66a74a23b60363a6993bed99d683`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214065218982b6113375606491ab1e634762ddca3ef5504388b1d3c6a1ac08c`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a64633e343063c6181b8f3ce93821d5b254c9e5f0a77263f25a7c0eb54a0b0`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294c219b884b9fd09349a24cc63f25d90265beb5881f638f0c09cb366e2bd622`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.1.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:a4c36fc1e6c3f05f62dd3df670c85649a01553185c648974b3032e776ecc9ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3ed1fb568a61057e0c783454f0fcc75a21c9e7cabab4f9af4c1ab6cd7414b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e11c7f979d544df66d02f8b3b68d4a0e4c6a4b1896a8e8feeedbf448902f81d`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 31.8 KB (31813 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.1.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:a1812991005eccfabfdc0716b625f330d285680c861e6007d54ad74e59038376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 MB (621187507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c752912932861ea9210e7c12b4a4f44415a6039d5a95eb49ae81c58512ab716`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bf66eb50e8cdc352eff12e1fead418e3a3069f2b2e1b344a29ba629e80aad`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 6.1 MB (6128819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ec91a8a8ab44c73e38b108b6051c0c41897a7053b0caea198d097c7408fcc`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304b9525db2a3ae82e431ea7618920d0656b09a5fcda75072fb8827e35f26cb`  
		Last Modified: Tue, 12 Nov 2024 01:25:01 GMT  
		Size: 589.1 MB (589080548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e7f1f525ddfd8ba3fb674f34e1da488c194c5ad1f91668a5e58026e5e75cb`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e232a340d660eaf24f630fc363a56a6ee6f56857c6ca27ac814e23966940aa3`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91989d7df9f972a800f38d69c3b7d9d75c8473fce3c5291ba58818a8cf085190`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99df0e555bfeec0a317a4b7a5de6d951b36f478df438ac0350779e07ed73a`  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb2faafb6c289081e19c8a37e45938c7e0451f3cab96fa7b0bd41decb162963`  
		Last Modified: Tue, 12 Nov 2024 01:24:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d3399400d923e4249292c833b72e5a635d8c8a4f5ccba6a78b1de6387d59f5`  
		Last Modified: Tue, 12 Nov 2024 01:24:51 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.1.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:7387d305d5f1917cf1c656d014a8b1bd9aad911777a073be61fdf8101e13c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (31983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f60df3c3ae69e504e3b73274cc5906fbb4f3327a5b010f53cd340284aaacf`

```dockerfile
```

-	Layers:
	-	`sha256:ab9f27b2d1466175015fad95fd3e806017463f7b7fedbf46377195b7b44fc701`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 32.0 KB (31983 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.6`

```console
$ docker pull couchbase@sha256:1dac0baa8d3aa50c8805d470251e7e7439b788dc65352a89b081946e8206ab91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4b58e0f8320f4bcaa514e02825a9f8b5e9b0db273b3aede57566531df5be959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650159192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483933a28486d97ddc44bbaa28bdf7ea70d9a3e4b677f7db49bd7c65ca6db17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce8dc623fb4f3b3e2f2cc90f532dac81793aacbfd9a8bc34c7f272703f7a04`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 6.2 MB (6203640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19b7a1a5cddb1dd4cc46227271aebc5b7e04e4a597533097f72215b6de729a9`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 864.1 KB (864102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254b5ffe8533432799b56c6292c531117f209ee875676174e3188c2cd6b67c76`  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e6bd39cd5ff83a20414e99f19041663a8313b4e0b5b69f78776e581d85181`  
		Last Modified: Tue, 12 Nov 2024 00:58:21 GMT  
		Size: 615.6 MB (615575393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d278f5fbb4ee15892c99cac6533847d979ee97e0e2b63098ca5edd4b181b0df`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d0cc313a835e05978d3a22e3dde75ae46d8d17a0e7db6fcdf13ed201b50cf`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159862f14c611065e1095187d03c984757591a20abe4438321678feb502d9abe`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8028c515492bf94343b675e5ffdf634023b92257b9ce84725ae8c515f7db4283`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6789d74bcbcf727c3b7a0b84ec13e12667d062fba4be39233407cc8ae5477`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ece909dec61e564cba6a304fe5fb8d33cb6caee4a492b8a6f3007f86f3044`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:07b7ddfcbbc6654d535c6f8e3aa740fc5686593c93e326761d5ca322ef7e456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6d9fe49c4d25b47cb627b75fba8083241e331d3cb80a914c8c43703509d432`

```dockerfile
```

-	Layers:
	-	`sha256:34e1cbdcc69402662d39f078751cc241871754e7f67167f99131512e449d1730`  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:7d6e356fbf2f30d7ae3b911cf30a838def123ad5cdc478f4c28ffc70e29b7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.1 MB (625088287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5969a5713480f17d7527249193f24bb3bc7ac4993aaab6b130a8b41df733d931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c396dd29f50bcc388cd0a519fac3f34e943a627c9613af69542b47bc466da9`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 6.0 MB (6041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d496ab92773d4bdd2c16f3738ba1c83e773a36e0751d0d35726afa7c5a8e82f`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 711.5 KB (711539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c75c5ebbbf48135024eccbbe96b521716a04200202d2875050b09064894d0`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319800ef44742b499fcfbc93d09de12fea172ea219d05d004f91261026c1c30`  
		Last Modified: Tue, 12 Nov 2024 01:21:19 GMT  
		Size: 592.4 MB (592356189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4482d826458e6222a04fe76268240d36790979884f96d96bb5b497326d52182`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274ccec6ea478230d9bcca8679cdf9aa16736185b4f153f0a55f9c0eb9d8681`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925dc1477caa9acc381dcf8926803bf1a1cdf324feebd4f41c09da0839e0645`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336c388f739dae1fd4292ccdf7c2ff11aadc5007eae6d45c269546dc0aba440`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365adc0efea529df15fec109eb02b13100a35d2ce7f790c19926d9dcebcb9b88`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f473ad2dfa83535574df9224f6c6e39650fac01ba4b6f717dfeb0cf4dbfb5f1`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:d6a3d2e1a5b12207764e6ba8007e41e07ca6c779a070cfd4927bc79370c17581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c65b08c9d54fe98556a645b20872297f9b7901d89dac7dad2fc39816b1d9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3800b8a1e257590c56d807e081dc422f2914c16ec2c2f9193abd124d3ef823d`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.4`

```console
$ docker pull couchbase@sha256:1712f7ea984a17e98422d23cad535a24251fc59726720a535786ea4386dfae77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:bb46e6473d51c1301c9e223d3b2a0f8bf9fda28282c59e1db26db3730d6cab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce6132cdb3fa96f599f385750800b1b5373663d2fee48a3c63a8d979f66cc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e4c8297c01db11c191858fd6cf8a7511d64a9118a1c1c750d681e3841e7f3`  
		Size: 39.3 MB (39298708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce06b3288eb688faca7cdc69d231f81faaa16e369004bfaef06068b9687c27a`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 926.1 KB (926065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee6a894c26a477744c2bc2b3101e65176887db8b0aeb5cf047c5884101d455`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7451ade6546d4e3b9d7953419d27c746ce6b0e9f23a891197a416e9a34cf29`  
		Last Modified: Wed, 11 Dec 2024 20:31:24 GMT  
		Size: 701.9 MB (701874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90a5eb80de27a57eeff0fead5cf60c6a688e1e8ab5d0510560b51277ea74a`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e05105422fbe68ce9e63c322db62cb0c03c6d6ce8d543b5923087760b80230`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b19bb06f3c79a6921855e7577dfa4a8a2ee0dbfef49e3ef3d13eb64eb62ac6`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b714361da7137396fe322b09fc0e45fedcb305b31525630b48039fbf83e968c`  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dba9ba6eea486f48865f659aa8f43797dd9892579171a4220ee34e9c387d3`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02364dd300798b3a2cdffb4fd4c9996710276b95ddd51cd92bf0bdb976c03`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:e875371520bedaa2baffb1beeea80adefa9df8a91ab6f12b0f01cc032977ad47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8101bc5a78ebb73c600b37b58d257e800de5275e2f26524dff7688415b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5951a1e0fc56cf41e206b54e13f281427ce397d604402be27b44f6c0664377aa`  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:51890184c7f5923841b5d2667eaac8968a0bb450d93b8e377e98f09867f21012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742534627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37c525e8fa9c00cf8205958c87d66908faf2e0ddb4182a09a3a6dddce05f1a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584481da729d18de66076f7754e37c2bbc39cbf05bd725b8aa1ebf12e1429a`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 38.8 MB (38844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9437b11152e6789daaee1b8b2816829ecec5fe6f7b7e66d2b57cf0a8fb340f5`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 770.4 KB (770448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b80241375276135ce691e34844832bbc260efe1e17f69b3f6c0c63a909cf8`  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3461cd28120e1f6e3a2a5d1632a4c0b55c34c9f983e76358764a1c2ef23dd3`  
		Last Modified: Wed, 11 Dec 2024 20:35:36 GMT  
		Size: 675.6 MB (675556548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9a2303e4b89e2749df948d7b77b504b000b4b505078adcfb37a62dcd836a2`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacce055b74872fa011424cec1d27c67e1a1e63bd686fd81dc6f607572c5a6bf`  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a8748af089af62557555c76fee8ee17283476c34a1a2719fce6c853545f9a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fd38386fb9ec7054edc75e6910d24e7f2828b2898eba07f0ab18f31df677a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18f583723b3303d32822f4967c9220fefebebdca459e5cbccd3efd1a0b5a6f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c5cb759bf8528349b284da7a8f8e541fdda4bec66b63b16482c7eca1d329f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:38911045564e44eee162d11ab29804f5a2411172e6c55fc0959d3046d87c3e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d54da9ce17575a870692837ab8c7c5ee9b37c2595580d3efb48953b68c80e`

```dockerfile
```

-	Layers:
	-	`sha256:f05cbd60b6824e37fba0b063111378fdd30aa399b050e17cc9fbeb37de5ea28d`  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community`

```console
$ docker pull couchbase@sha256:f1adb86d7cbd80d8dbacd3f07fc0889e04dc066f482c074c699916257df8452a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:734d65f9237d4b450de5ae67135b4eaeac9b93fb732d523091821d9ca990c7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396856400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0728fa92614e27d1fff830a23e35aa4b80767586c029d7108aa0a9467f4529b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:05:07 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:05:07 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:05:07 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:05:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:05:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:05:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b733c0871caa9a475d215b92cbe37a613e1fcdbccb1b7bcc3afcae3a5f468a`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 6.2 MB (6203660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62305e070fed67cd0548459a868e5951da2c6de93092828d660433a17b16029`  
		Last Modified: Tue, 12 Nov 2024 00:56:46 GMT  
		Size: 864.1 KB (864119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21607cc5c773a16308ddb3a486d8f3323e7334271486a1a796f4995653967743`  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fddb1102a33b33a1703a410e4440b66334d248a5a0d1881f003b071c88854f`  
		Last Modified: Tue, 12 Nov 2024 00:56:59 GMT  
		Size: 362.3 MB (362272565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b327ae54827ef79a854d0a745bd151ce3bcdf468be38c080542ecd06f9e0e`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746b2dd4b873da687238d40aae68b28b0be0378fa18f57b28c4e2d323b5ae335`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105130c90e1d7094a2b5da46bc7354108466818317ece4ad1b3f061e7f4d98e4`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f530646a8ed8e8a11335816a224f1c34c924412c2827d05cf0680ed20f6df772`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c81daafc67e7c37c3bfb30cb021ef86ea144942d2f49695f289245d3d56003`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce18c6e915edfcaa8eccbe37468315666964179ac85f90a9e1103a5369545b3`  
		Last Modified: Tue, 12 Nov 2024 00:56:49 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community` - unknown; unknown

```console
$ docker pull couchbase@sha256:306b63aef21099f06466ca02a915a2a140a989f4f0d35142bdbf51889b538348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec4fb915b799a8c6c78cb52d58c21e6cef7f08666cd2ab17479a19e63a08210`

```dockerfile
```

-	Layers:
	-	`sha256:2ec97e150fe65dd5e37aae67664b9a278c0a3f27f53ca4d4d430ebc3c55f6aca`  
		Last Modified: Tue, 12 Nov 2024 00:56:45 GMT  
		Size: 35.8 KB (35802 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:58b172719e2896d56371c0979b68d1a939bee50519877c374e334841b3cf36ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374267184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad90b83dc7735a300f107f9fa8dc1db852f0286d864bc835fd2f46f8f0fbd2e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:05:07 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:05:07 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:05:07 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:05:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:05:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:05:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2d226b8a2a5bed7e39fdd186b0130b1e137e9c1e042bebfd75a673998138b6`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 6.0 MB (6041697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acfedf2947d1ad202b22f7276f9292046ade1b3bf08392056597fb098b4415`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 711.5 KB (711511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88b570ce0d0123eb3ccdb4b164753247a71923e6815f043d834e220033c51b`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07042fae3f2858dcdd21687a650931f8a79d20eb8103bd8dc990443220c333e`  
		Size: 341.5 MB (341535132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f38b13293c7d7844aeb9cfcf70a63d5eaca157977303e09697bf020b7cacfe9`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07a6d2c9db9ce42ca8d4e4b31c35d7e5826f362d895f6167ebd7049c6ca2aa`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc516eae03b66fcc21e81d3d956f7a7886fd0bfe3b3d1b5cc6dfd7dc584987c`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897ed6965fec2096defec1cd8db1ce5070bebe67e8fbda48d0d4e705ccc052b2`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7086d6272eff2099f81d5daea3de53060873ab4e43d02d5754ac0bba56512bf4`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535d59683aff16aebf534a487ac4324548dd435638c4ddc7e63d4764ab571a83`  
		Last Modified: Tue, 12 Nov 2024 01:18:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community` - unknown; unknown

```console
$ docker pull couchbase@sha256:ca6a7c009639b29a6e72fccae3f2a6f7084dae7d09ad263d10c8bd5d66c9f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f2bf5ae98b097b085ec5d5701d85cf57d63ace6314c139bd04c073e1d70c43`

```dockerfile
```

-	Layers:
	-	`sha256:22722e4310d9de112ec3a5fbc00a7349c38061faab4b2422942248924a9977bb`  
		Size: 36.0 KB (35987 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:19698d38ea39a37df127b8aedc8a0a636e6b70d05dac2ff8ae8bd7eb23367bfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:a7f57dfc5af064429d924a9923c182bc8c6daa741a35a30802e10287e8ce0b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427793634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d0199cea5f0542b1193febe89a7d0c75b8043dcaf5420b6f999ced324627a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_VERSION=7.0.2
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11211/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa34ea4c5838f19cbd98dae13bb1ebf7424ae31d4fa4590d50d99044d50eb0c`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 6.3 MB (6309006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4be9e11bfb8db841d9da9272d474f86cb7873ab22aecab7fd69ee3d215ea89`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c5a92dde3ee759527e7abefba8c3c9f1a47617e86c2e6130f7faf8daa4f154`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a774f6cc61f43318b53b9150c419589ee1c26097cf86a669c99d6866658bbe`  
		Last Modified: Tue, 12 Nov 2024 00:57:29 GMT  
		Size: 393.8 MB (393839665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5338fd01715c169985f29512ae5aebf54a7c5646c559613d8be8d23a23d3370`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7704e91a72f65a6a7811eb71b9fd0e8285024c4e2996765e2ec0e53410134e`  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db5118e35dcc31edb5b6005cd82524262d31733011db37b8ff8f1012475e5cf`  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24303daae360530b91f217860cad9c71d4659594cdb57ec284e6655f83f26027`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b8c0fed36ec953e86d42dfdd4ab28be5810066256b2d7d1215a4dda91d07c`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3111960e4b3acbcd9dd9c2cbd2cd905af8ccdf7850d1a6561c778c4cd46585`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 129.5 KB (129508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5937e8f6cb192665e2d8e41ccfdc2e382c4d2f3b85820bed0dd7d32b547e58`  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.0.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:59a9821fe624b203e75f9940728016efbe6735a0725ba74f8cffa686eb05a92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d856f7f5bc88b5ed4ae470f8d3f1ed0afb40ef7a362630c3e3207dee920bfa28`

```dockerfile
```

-	Layers:
	-	`sha256:3c5c87f748204cec1ed6a552e05685bab995305b0be8422bc5b2f74f4942f90b`  
		Size: 31.2 KB (31249 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.1.1`

```console
$ docker pull couchbase@sha256:a423306458bb40343dcbf2acb90822a8e3156120c65718f00085d95f2a2d703a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.1.1` - linux; amd64

```console
$ docker pull couchbase@sha256:833e567660bc11f0e12adfa89920c29e26b87417722bc5c8c2f16eca405e5f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345394027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cf3f0bf4aa8617f98f65b436524bc44498c46f40855a0f2ed2895be25e4a92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11211/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ceeb4e185cf17dcfbd76202d41b1f779059db2b1c4f25f7fd8954f4b34fafd1`  
		Last Modified: Tue, 12 Nov 2024 00:57:10 GMT  
		Size: 6.3 MB (6299184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db54cebafa4938d3d7b4ee25b297e9eb14bca6a9de8a756c0cb04645d41939d`  
		Last Modified: Tue, 12 Nov 2024 00:57:10 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b0d134c3b1fb182d2e0d3bb22a9b752db9af685125ce571029872e65d1452`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 311.6 MB (311579478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5bc71e0bf92574e9d3450164ff9cc7ef5834d9b829a3a49abf5edd1ea861d3`  
		Last Modified: Tue, 12 Nov 2024 00:57:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e51bbcfa9640f6c07a7b28d0525f2e469114a0579c8fb4083c237d9ebc93c2`  
		Last Modified: Tue, 12 Nov 2024 00:57:11 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9205991fdd2e04a36a59fa535bc608d1eb3880060c791f3a2d79be9b5e15`  
		Last Modified: Tue, 12 Nov 2024 00:57:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111d2c6cbe9881d78ce3723e59eecf742971d74f12f636ae3f5c8f31913c659a`  
		Last Modified: Tue, 12 Nov 2024 00:57:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafb32c5c5d80acf3f43306845fe4a87701eb0809b1c2fde4b42d1f82f2ea908`  
		Last Modified: Tue, 12 Nov 2024 00:57:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eadb8b1fa1269ba9cfb39614acc96a904567c3056928fe7d6cdf20347cddad`  
		Last Modified: Tue, 12 Nov 2024 00:57:12 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.1.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:cc7a0d8c9b8d1c7d89028f71c4bf0ce42115bf9a691763543875ed90b618b7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93110381a41301c77730cdaed111f10b0cbe55fefb2db1a9accdfac484f4c5bb`

```dockerfile
```

-	Layers:
	-	`sha256:1309c973f2523ad10063ae9e5dab51ba4ac5082c4b443ad55eec0dff4cd6c9c1`  
		Last Modified: Tue, 12 Nov 2024 00:57:10 GMT  
		Size: 31.0 KB (30979 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.1.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:c0af1fc307a41e31c30159ac1f8cb6b5e17ddee47f7402a2c9248d0b13a88d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325904624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0559da32bc1c988c2d1c54a1d38514c714b12c8b394d7506e7c3bb80d1879fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11211/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e419e16c8ab3f43fb2e52fa1ba0754f15791c4425990295e17cfd17cd375024`  
		Size: 6.1 MB (6128917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8c90aaa1f5f80b5f71a315f821261902c0c58079c49b7f1a30eaa84793c05f`  
		Last Modified: Tue, 12 Nov 2024 01:26:29 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c601b56297f6edd59be6e756c0a993cf32fe38982037ced4332963c04c67ee`  
		Last Modified: Tue, 12 Nov 2024 01:26:36 GMT  
		Size: 293.8 MB (293797569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ae7027a29c4e3c8af7de8f8994afaa9f4a856a6b013d91ba4a902fa439af8`  
		Last Modified: Tue, 12 Nov 2024 01:26:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2547f94f71653fe4d3977fe5144a73cdca9b6322dc980abe6b939fb9b2651fdb`  
		Last Modified: Tue, 12 Nov 2024 01:26:30 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac90046bfeabf6a0980821846e8555ad3d2f4bf6ec352172c55ae67448daff`  
		Last Modified: Tue, 12 Nov 2024 01:26:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923c7d2b70be634f64891fa4c4f3d1d9337c9ca19b3064356184c8ab2c3eb6d`  
		Last Modified: Tue, 12 Nov 2024 01:26:31 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e04cb9c863ea03e6bedbd21197534afa56d6f5d6f74866e9e1e23ae915389`  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b16145cdc4499697a45897d5a77dd302660318199032646f8be804f9b0078f`  
		Last Modified: Tue, 12 Nov 2024 01:26:31 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.1.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:0ee5e890c71d90cd7bf3941c042ecd792256919a2ea29d518ffe14c433cd3916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 KB (31137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611560ae8b18ef3267595620a84617d84cfea6d3d9fed81aa71b9d58c2a87a9`

```dockerfile
```

-	Layers:
	-	`sha256:d0f49fe2faebcc583a63536fcb072f338e0abde849cf5bb95ab0fe289287a04b`  
		Last Modified: Tue, 12 Nov 2024 01:26:29 GMT  
		Size: 31.1 KB (31137 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:d11bf54e681306bb46c892aa587a2d7005eb4f0865d2f50ecf4d1f1269935a07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:25c1a39c2c8ccaf5c62795f6dd12aaece6917c525b947df0bb7e9194b9a6646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364888406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d643c72b83d8e2584ca061927edb83473099ec79136161b1ad70b62314822b32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1249f821f7cc033833e49bccee2b7e3ab0ce3e339b0f8a6d8b572ad7b14bb9a7`  
		Last Modified: Tue, 12 Nov 2024 00:57:19 GMT  
		Size: 6.3 MB (6299169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a9107d36a345fcb6cfae794e4f7b9b725a40316513d0c069df3904e1076f6`  
		Last Modified: Tue, 12 Nov 2024 00:57:18 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ce8de9a95b31a3a4ccdf80d3c544a6f82cca983645911a87d8f093385cde9`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 331.1 MB (331073871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552b6419f103c9228fc0d828d34336fe1f6dd4b7fdd88b69279b876ded02822e`  
		Last Modified: Tue, 12 Nov 2024 00:57:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9430f310a775f4143ef2c28f618b6135eebdc3e5a41478ab1ff73577291a02ef`  
		Last Modified: Tue, 12 Nov 2024 00:57:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45825920c7cc2223a1ccf5209c5b14eb7093f11436a929d818f1f6fbc7e566c`  
		Last Modified: Tue, 12 Nov 2024 00:57:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913574a0bf2ab74f73adc3b1a2b812c78a2cb37a7666ad18441c8359e19590fc`  
		Last Modified: Tue, 12 Nov 2024 00:57:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c2e751e345d362ad129af7c338f7fc75acc0a3e67ec3a955dd2a4dcd2366f`  
		Last Modified: Tue, 12 Nov 2024 00:57:21 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137158146c83890791c53f554fa1c73f9de0bde771c5fbc3f2867bff9a9550f9`  
		Last Modified: Tue, 12 Nov 2024 00:57:21 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:31f7220e99398dbd08300a471e4dbcba1f52909eef49529f43ab0fce530ca06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f2844420556df11febba9e496df8f473c36d07e513c08b5a3651d0dc3a806c`

```dockerfile
```

-	Layers:
	-	`sha256:213753f0bbe49850ddeff4494ec08e34a9d7f0fc31cb26b310c0deaa1ecb3820`  
		Last Modified: Tue, 12 Nov 2024 00:57:18 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:0601e812e45f7c556dabb6ba9a246d00c6f1f220a33a05bba08f1f1ead5af6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344968826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45191f1f54e7e792276513dc3abbe9bcfef9673cd557b38d6cc160a0f2d34c43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a87bfd0a7181920474e87c7920879cc89e906ca81559bad045f9294c33d7d0`  
		Last Modified: Tue, 12 Nov 2024 01:22:56 GMT  
		Size: 6.1 MB (6128843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b1a14c7dd6c90b90d1abaf9287cfd7d2b79bad7e250fdec20e18521b55cccd`  
		Last Modified: Tue, 12 Nov 2024 01:22:55 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64baeab963456e940d34f69de18e2781940319ee2dafdd23ff36de78a23a22`  
		Last Modified: Tue, 12 Nov 2024 01:23:03 GMT  
		Size: 312.9 MB (312861847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b10af300674dbd4168b82a862df679d8dbb579c01f6cc075ad4aa28551c19cd`  
		Last Modified: Tue, 12 Nov 2024 01:22:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186d2adce589e4cf8ac6c070aa6ee61e5eb541419746737ac3cd48fc799eb36`  
		Last Modified: Tue, 12 Nov 2024 01:22:56 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20636096e3990aab6dacf5e9273bcaccb11db9586ab25dfea2654f3b136f644e`  
		Last Modified: Tue, 12 Nov 2024 01:22:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9d6d9e2e7c426ba012bfd436979f3e6e671ba39bda68dd9f6afddc014679`  
		Last Modified: Tue, 12 Nov 2024 01:22:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f5593ec9b92ce6ae6002908a906a71c2838037b13a91c4b9b783fc7b47f34`  
		Last Modified: Tue, 12 Nov 2024 01:22:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41887c42971b90c60bd0e3b23b4110464c025f2962d76ec7b892b0cc8312ce`  
		Last Modified: Tue, 12 Nov 2024 01:22:57 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:2f148f15afc46d18e37f6e34c00346b4a026f65aa4de9a9dfc5beefa7d50c884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbd53f0b4cc44d7189d302fd986468a42e942990d798485674874fff6950c95`

```dockerfile
```

-	Layers:
	-	`sha256:a4215aaf563e48f52f620526422120bffa2d27f162e61b24631fa1b67351473b`  
		Last Modified: Tue, 12 Nov 2024 01:22:55 GMT  
		Size: 31.7 KB (31658 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.6.2`

```console
$ docker pull couchbase@sha256:f1adb86d7cbd80d8dbacd3f07fc0889e04dc066f482c074c699916257df8452a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:734d65f9237d4b450de5ae67135b4eaeac9b93fb732d523091821d9ca990c7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396856400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0728fa92614e27d1fff830a23e35aa4b80767586c029d7108aa0a9467f4529b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:05:07 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:05:07 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:05:07 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:05:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:05:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:05:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b733c0871caa9a475d215b92cbe37a613e1fcdbccb1b7bcc3afcae3a5f468a`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 6.2 MB (6203660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62305e070fed67cd0548459a868e5951da2c6de93092828d660433a17b16029`  
		Last Modified: Tue, 12 Nov 2024 00:56:46 GMT  
		Size: 864.1 KB (864119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21607cc5c773a16308ddb3a486d8f3323e7334271486a1a796f4995653967743`  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fddb1102a33b33a1703a410e4440b66334d248a5a0d1881f003b071c88854f`  
		Last Modified: Tue, 12 Nov 2024 00:56:59 GMT  
		Size: 362.3 MB (362272565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b327ae54827ef79a854d0a745bd151ce3bcdf468be38c080542ecd06f9e0e`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746b2dd4b873da687238d40aae68b28b0be0378fa18f57b28c4e2d323b5ae335`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105130c90e1d7094a2b5da46bc7354108466818317ece4ad1b3f061e7f4d98e4`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f530646a8ed8e8a11335816a224f1c34c924412c2827d05cf0680ed20f6df772`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c81daafc67e7c37c3bfb30cb021ef86ea144942d2f49695f289245d3d56003`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce18c6e915edfcaa8eccbe37468315666964179ac85f90a9e1103a5369545b3`  
		Last Modified: Tue, 12 Nov 2024 00:56:49 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:306b63aef21099f06466ca02a915a2a140a989f4f0d35142bdbf51889b538348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec4fb915b799a8c6c78cb52d58c21e6cef7f08666cd2ab17479a19e63a08210`

```dockerfile
```

-	Layers:
	-	`sha256:2ec97e150fe65dd5e37aae67664b9a278c0a3f27f53ca4d4d430ebc3c55f6aca`  
		Last Modified: Tue, 12 Nov 2024 00:56:45 GMT  
		Size: 35.8 KB (35802 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:58b172719e2896d56371c0979b68d1a939bee50519877c374e334841b3cf36ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374267184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad90b83dc7735a300f107f9fa8dc1db852f0286d864bc835fd2f46f8f0fbd2e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:05:07 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:05:07 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:05:07 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:05:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:05:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:05:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2d226b8a2a5bed7e39fdd186b0130b1e137e9c1e042bebfd75a673998138b6`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 6.0 MB (6041697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acfedf2947d1ad202b22f7276f9292046ade1b3bf08392056597fb098b4415`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 711.5 KB (711511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88b570ce0d0123eb3ccdb4b164753247a71923e6815f043d834e220033c51b`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07042fae3f2858dcdd21687a650931f8a79d20eb8103bd8dc990443220c333e`  
		Size: 341.5 MB (341535132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f38b13293c7d7844aeb9cfcf70a63d5eaca157977303e09697bf020b7cacfe9`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07a6d2c9db9ce42ca8d4e4b31c35d7e5826f362d895f6167ebd7049c6ca2aa`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc516eae03b66fcc21e81d3d956f7a7886fd0bfe3b3d1b5cc6dfd7dc584987c`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897ed6965fec2096defec1cd8db1ce5070bebe67e8fbda48d0d4e705ccc052b2`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7086d6272eff2099f81d5daea3de53060873ab4e43d02d5754ac0bba56512bf4`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535d59683aff16aebf534a487ac4324548dd435638c4ddc7e63d4764ab571a83`  
		Last Modified: Tue, 12 Nov 2024 01:18:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:ca6a7c009639b29a6e72fccae3f2a6f7084dae7d09ad263d10c8bd5d66c9f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f2bf5ae98b097b085ec5d5701d85cf57d63ace6314c139bd04c073e1d70c43`

```dockerfile
```

-	Layers:
	-	`sha256:22722e4310d9de112ec3a5fbc00a7349c38061faab4b2422942248924a9977bb`  
		Size: 36.0 KB (35987 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:1712f7ea984a17e98422d23cad535a24251fc59726720a535786ea4386dfae77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:bb46e6473d51c1301c9e223d3b2a0f8bf9fda28282c59e1db26db3730d6cab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce6132cdb3fa96f599f385750800b1b5373663d2fee48a3c63a8d979f66cc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e4c8297c01db11c191858fd6cf8a7511d64a9118a1c1c750d681e3841e7f3`  
		Size: 39.3 MB (39298708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce06b3288eb688faca7cdc69d231f81faaa16e369004bfaef06068b9687c27a`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 926.1 KB (926065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee6a894c26a477744c2bc2b3101e65176887db8b0aeb5cf047c5884101d455`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7451ade6546d4e3b9d7953419d27c746ce6b0e9f23a891197a416e9a34cf29`  
		Last Modified: Wed, 11 Dec 2024 20:31:24 GMT  
		Size: 701.9 MB (701874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90a5eb80de27a57eeff0fead5cf60c6a688e1e8ab5d0510560b51277ea74a`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e05105422fbe68ce9e63c322db62cb0c03c6d6ce8d543b5923087760b80230`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b19bb06f3c79a6921855e7577dfa4a8a2ee0dbfef49e3ef3d13eb64eb62ac6`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b714361da7137396fe322b09fc0e45fedcb305b31525630b48039fbf83e968c`  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dba9ba6eea486f48865f659aa8f43797dd9892579171a4220ee34e9c387d3`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02364dd300798b3a2cdffb4fd4c9996710276b95ddd51cd92bf0bdb976c03`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:e875371520bedaa2baffb1beeea80adefa9df8a91ab6f12b0f01cc032977ad47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8101bc5a78ebb73c600b37b58d257e800de5275e2f26524dff7688415b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5951a1e0fc56cf41e206b54e13f281427ce397d604402be27b44f6c0664377aa`  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:51890184c7f5923841b5d2667eaac8968a0bb450d93b8e377e98f09867f21012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742534627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37c525e8fa9c00cf8205958c87d66908faf2e0ddb4182a09a3a6dddce05f1a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584481da729d18de66076f7754e37c2bbc39cbf05bd725b8aa1ebf12e1429a`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 38.8 MB (38844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9437b11152e6789daaee1b8b2816829ecec5fe6f7b7e66d2b57cf0a8fb340f5`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 770.4 KB (770448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b80241375276135ce691e34844832bbc260efe1e17f69b3f6c0c63a909cf8`  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3461cd28120e1f6e3a2a5d1632a4c0b55c34c9f983e76358764a1c2ef23dd3`  
		Last Modified: Wed, 11 Dec 2024 20:35:36 GMT  
		Size: 675.6 MB (675556548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9a2303e4b89e2749df948d7b77b504b000b4b505078adcfb37a62dcd836a2`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacce055b74872fa011424cec1d27c67e1a1e63bd686fd81dc6f607572c5a6bf`  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a8748af089af62557555c76fee8ee17283476c34a1a2719fce6c853545f9a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fd38386fb9ec7054edc75e6910d24e7f2828b2898eba07f0ab18f31df677a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18f583723b3303d32822f4967c9220fefebebdca459e5cbccd3efd1a0b5a6f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c5cb759bf8528349b284da7a8f8e541fdda4bec66b63b16482c7eca1d329f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:38911045564e44eee162d11ab29804f5a2411172e6c55fc0959d3046d87c3e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d54da9ce17575a870692837ab8c7c5ee9b37c2595580d3efb48953b68c80e`

```dockerfile
```

-	Layers:
	-	`sha256:f05cbd60b6824e37fba0b063111378fdd30aa399b050e17cc9fbeb37de5ea28d`  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.0.5`

```console
$ docker pull couchbase@sha256:60c8ccd24f777fe39ff9efc279d2be4d06d3b16a25d44ea9ba6c0953758e6607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchbase:enterprise-7.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:60e2a7c09d0ff030dc539ca343adabf08a5f82a68dd6116615ba4ae3c953dea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.4 MB (615421160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026745745bfc815225fc02520deb37c093b0bd428e52391c582783e3eed27025`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe1ca44819ce1f6620cdda7080ff7d0d00ab67bdd4d617046725fb60c37a0a`  
		Last Modified: Tue, 12 Nov 2024 00:57:56 GMT  
		Size: 6.3 MB (6299140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da62334b6d5935e1d2a21e75d4a90660d2a6ce9feaa3e4f8c308d92e2997c5a`  
		Last Modified: Tue, 12 Nov 2024 00:57:55 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2812246da48a667f0f533a58a1d53d9329d02316879be4bbbe44d28e3aeb333d`  
		Last Modified: Tue, 12 Nov 2024 00:58:08 GMT  
		Size: 581.6 MB (581606645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f12568e81669c3486dfefd3a7ec4251a7502beaef457d25b6cd8073431ed8`  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1ef0f44e68c300f1b04ffda254e09257c2150fcbbf5cbe979646878a86d57`  
		Last Modified: Tue, 12 Nov 2024 00:57:56 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8731368a59d5ffc85e090fbf063db28fa568ba90bf829199413abc0e88931d79`  
		Last Modified: Tue, 12 Nov 2024 00:57:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cba7f2fc85eb14a8ef77fbbb3efa0e7b64132f2856e22b3c5e2351884c502f4`  
		Last Modified: Tue, 12 Nov 2024 00:57:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3a70bf740ffde435aad8b4f4ec9f9418c4ef0b1610fb10dfe7e952f6c8062`  
		Last Modified: Tue, 12 Nov 2024 00:57:57 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4415972b5950cb7d95b8c95a3cd363dd571eb483d08ed7b481c7558b8619d84d`  
		Last Modified: Tue, 12 Nov 2024 00:57:57 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.0.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:407c6dc9a9899fdf806edcc66b01ebd5b970d34a24e09049f5d459ef98113b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866f35aa2740a6df461d16c3bd389b4e16fc77aa94b97d21362f67396d7c477e`

```dockerfile
```

-	Layers:
	-	`sha256:452aaa5b1049883bfb1688c7f984bd35b27bac79e7da69c10357ea1c8de38e7c`  
		Last Modified: Tue, 12 Nov 2024 00:57:55 GMT  
		Size: 31.0 KB (31010 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.1.6`

```console
$ docker pull couchbase@sha256:caaffdc32520e19d03e313cf8f54db669d66a4dcc305d01c47d7f07fcb013485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:f6fbfea040c78f888b1b371de3af6c2ab9d7a3e61802a191ea49cdae564621eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650734358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d966266515710c09ca1890e71d9b6b0d607ba26c42a75cb7a82ba286fe02b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8afbf2f1c19b5c3d3c4cbe897177ce3c9840d161fc0565a3c6efab784eb292f`  
		Size: 6.3 MB (6299173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400bc3fbd7c94e788acf49bf00e316d1fcd9b182010d90c30381eae089bc06bb`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c89ce562297e58a96cd81b8b1fe5443d7b6ff2b214d58811cada4e2e83db8`  
		Last Modified: Tue, 12 Nov 2024 00:58:22 GMT  
		Size: 616.9 MB (616919823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae46418d8da2075f00a6844dabd34032253c4a34143808208e0077ea08f6b96d`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c4ca65edb4e0fa9d1ca9147de9136660a5418572cb221bfdcf3e59a1750e8f`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8eccd799a40e46d685be5d2f321899fbc66a74a23b60363a6993bed99d683`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214065218982b6113375606491ab1e634762ddca3ef5504388b1d3c6a1ac08c`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a64633e343063c6181b8f3ce93821d5b254c9e5f0a77263f25a7c0eb54a0b0`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294c219b884b9fd09349a24cc63f25d90265beb5881f638f0c09cb366e2bd622`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.1.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:a4c36fc1e6c3f05f62dd3df670c85649a01553185c648974b3032e776ecc9ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3ed1fb568a61057e0c783454f0fcc75a21c9e7cabab4f9af4c1ab6cd7414b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e11c7f979d544df66d02f8b3b68d4a0e4c6a4b1896a8e8feeedbf448902f81d`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 31.8 KB (31813 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.1.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:a1812991005eccfabfdc0716b625f330d285680c861e6007d54ad74e59038376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 MB (621187507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c752912932861ea9210e7c12b4a4f44415a6039d5a95eb49ae81c58512ab716`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bf66eb50e8cdc352eff12e1fead418e3a3069f2b2e1b344a29ba629e80aad`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 6.1 MB (6128819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ec91a8a8ab44c73e38b108b6051c0c41897a7053b0caea198d097c7408fcc`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304b9525db2a3ae82e431ea7618920d0656b09a5fcda75072fb8827e35f26cb`  
		Last Modified: Tue, 12 Nov 2024 01:25:01 GMT  
		Size: 589.1 MB (589080548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e7f1f525ddfd8ba3fb674f34e1da488c194c5ad1f91668a5e58026e5e75cb`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e232a340d660eaf24f630fc363a56a6ee6f56857c6ca27ac814e23966940aa3`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91989d7df9f972a800f38d69c3b7d9d75c8473fce3c5291ba58818a8cf085190`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99df0e555bfeec0a317a4b7a5de6d951b36f478df438ac0350779e07ed73a`  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb2faafb6c289081e19c8a37e45938c7e0451f3cab96fa7b0bd41decb162963`  
		Last Modified: Tue, 12 Nov 2024 01:24:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d3399400d923e4249292c833b72e5a635d8c8a4f5ccba6a78b1de6387d59f5`  
		Last Modified: Tue, 12 Nov 2024 01:24:51 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.1.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:7387d305d5f1917cf1c656d014a8b1bd9aad911777a073be61fdf8101e13c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (31983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f60df3c3ae69e504e3b73274cc5906fbb4f3327a5b010f53cd340284aaacf`

```dockerfile
```

-	Layers:
	-	`sha256:ab9f27b2d1466175015fad95fd3e806017463f7b7fedbf46377195b7b44fc701`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 32.0 KB (31983 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.6`

```console
$ docker pull couchbase@sha256:1dac0baa8d3aa50c8805d470251e7e7439b788dc65352a89b081946e8206ab91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4b58e0f8320f4bcaa514e02825a9f8b5e9b0db273b3aede57566531df5be959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650159192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483933a28486d97ddc44bbaa28bdf7ea70d9a3e4b677f7db49bd7c65ca6db17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce8dc623fb4f3b3e2f2cc90f532dac81793aacbfd9a8bc34c7f272703f7a04`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 6.2 MB (6203640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19b7a1a5cddb1dd4cc46227271aebc5b7e04e4a597533097f72215b6de729a9`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 864.1 KB (864102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254b5ffe8533432799b56c6292c531117f209ee875676174e3188c2cd6b67c76`  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e6bd39cd5ff83a20414e99f19041663a8313b4e0b5b69f78776e581d85181`  
		Last Modified: Tue, 12 Nov 2024 00:58:21 GMT  
		Size: 615.6 MB (615575393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d278f5fbb4ee15892c99cac6533847d979ee97e0e2b63098ca5edd4b181b0df`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d0cc313a835e05978d3a22e3dde75ae46d8d17a0e7db6fcdf13ed201b50cf`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159862f14c611065e1095187d03c984757591a20abe4438321678feb502d9abe`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8028c515492bf94343b675e5ffdf634023b92257b9ce84725ae8c515f7db4283`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6789d74bcbcf727c3b7a0b84ec13e12667d062fba4be39233407cc8ae5477`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ece909dec61e564cba6a304fe5fb8d33cb6caee4a492b8a6f3007f86f3044`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:07b7ddfcbbc6654d535c6f8e3aa740fc5686593c93e326761d5ca322ef7e456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6d9fe49c4d25b47cb627b75fba8083241e331d3cb80a914c8c43703509d432`

```dockerfile
```

-	Layers:
	-	`sha256:34e1cbdcc69402662d39f078751cc241871754e7f67167f99131512e449d1730`  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:7d6e356fbf2f30d7ae3b911cf30a838def123ad5cdc478f4c28ffc70e29b7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.1 MB (625088287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5969a5713480f17d7527249193f24bb3bc7ac4993aaab6b130a8b41df733d931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c396dd29f50bcc388cd0a519fac3f34e943a627c9613af69542b47bc466da9`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 6.0 MB (6041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d496ab92773d4bdd2c16f3738ba1c83e773a36e0751d0d35726afa7c5a8e82f`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 711.5 KB (711539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c75c5ebbbf48135024eccbbe96b521716a04200202d2875050b09064894d0`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319800ef44742b499fcfbc93d09de12fea172ea219d05d004f91261026c1c30`  
		Last Modified: Tue, 12 Nov 2024 01:21:19 GMT  
		Size: 592.4 MB (592356189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4482d826458e6222a04fe76268240d36790979884f96d96bb5b497326d52182`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274ccec6ea478230d9bcca8679cdf9aa16736185b4f153f0a55f9c0eb9d8681`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925dc1477caa9acc381dcf8926803bf1a1cdf324feebd4f41c09da0839e0645`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336c388f739dae1fd4292ccdf7c2ff11aadc5007eae6d45c269546dc0aba440`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365adc0efea529df15fec109eb02b13100a35d2ce7f790c19926d9dcebcb9b88`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f473ad2dfa83535574df9224f6c6e39650fac01ba4b6f717dfeb0cf4dbfb5f1`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:d6a3d2e1a5b12207764e6ba8007e41e07ca6c779a070cfd4927bc79370c17581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c65b08c9d54fe98556a645b20872297f9b7901d89dac7dad2fc39816b1d9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3800b8a1e257590c56d807e081dc422f2914c16ec2c2f9193abd124d3ef823d`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.4`

```console
$ docker pull couchbase@sha256:1712f7ea984a17e98422d23cad535a24251fc59726720a535786ea4386dfae77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:bb46e6473d51c1301c9e223d3b2a0f8bf9fda28282c59e1db26db3730d6cab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce6132cdb3fa96f599f385750800b1b5373663d2fee48a3c63a8d979f66cc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e4c8297c01db11c191858fd6cf8a7511d64a9118a1c1c750d681e3841e7f3`  
		Size: 39.3 MB (39298708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce06b3288eb688faca7cdc69d231f81faaa16e369004bfaef06068b9687c27a`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 926.1 KB (926065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee6a894c26a477744c2bc2b3101e65176887db8b0aeb5cf047c5884101d455`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7451ade6546d4e3b9d7953419d27c746ce6b0e9f23a891197a416e9a34cf29`  
		Last Modified: Wed, 11 Dec 2024 20:31:24 GMT  
		Size: 701.9 MB (701874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90a5eb80de27a57eeff0fead5cf60c6a688e1e8ab5d0510560b51277ea74a`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e05105422fbe68ce9e63c322db62cb0c03c6d6ce8d543b5923087760b80230`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b19bb06f3c79a6921855e7577dfa4a8a2ee0dbfef49e3ef3d13eb64eb62ac6`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b714361da7137396fe322b09fc0e45fedcb305b31525630b48039fbf83e968c`  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dba9ba6eea486f48865f659aa8f43797dd9892579171a4220ee34e9c387d3`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02364dd300798b3a2cdffb4fd4c9996710276b95ddd51cd92bf0bdb976c03`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:e875371520bedaa2baffb1beeea80adefa9df8a91ab6f12b0f01cc032977ad47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8101bc5a78ebb73c600b37b58d257e800de5275e2f26524dff7688415b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5951a1e0fc56cf41e206b54e13f281427ce397d604402be27b44f6c0664377aa`  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:51890184c7f5923841b5d2667eaac8968a0bb450d93b8e377e98f09867f21012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742534627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37c525e8fa9c00cf8205958c87d66908faf2e0ddb4182a09a3a6dddce05f1a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584481da729d18de66076f7754e37c2bbc39cbf05bd725b8aa1ebf12e1429a`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 38.8 MB (38844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9437b11152e6789daaee1b8b2816829ecec5fe6f7b7e66d2b57cf0a8fb340f5`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 770.4 KB (770448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b80241375276135ce691e34844832bbc260efe1e17f69b3f6c0c63a909cf8`  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3461cd28120e1f6e3a2a5d1632a4c0b55c34c9f983e76358764a1c2ef23dd3`  
		Last Modified: Wed, 11 Dec 2024 20:35:36 GMT  
		Size: 675.6 MB (675556548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9a2303e4b89e2749df948d7b77b504b000b4b505078adcfb37a62dcd836a2`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacce055b74872fa011424cec1d27c67e1a1e63bd686fd81dc6f607572c5a6bf`  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a8748af089af62557555c76fee8ee17283476c34a1a2719fce6c853545f9a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fd38386fb9ec7054edc75e6910d24e7f2828b2898eba07f0ab18f31df677a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18f583723b3303d32822f4967c9220fefebebdca459e5cbccd3efd1a0b5a6f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c5cb759bf8528349b284da7a8f8e541fdda4bec66b63b16482c7eca1d329f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:38911045564e44eee162d11ab29804f5a2411172e6c55fc0959d3046d87c3e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d54da9ce17575a870692837ab8c7c5ee9b37c2595580d3efb48953b68c80e`

```dockerfile
```

-	Layers:
	-	`sha256:f05cbd60b6824e37fba0b063111378fdd30aa399b050e17cc9fbeb37de5ea28d`  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:1712f7ea984a17e98422d23cad535a24251fc59726720a535786ea4386dfae77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:bb46e6473d51c1301c9e223d3b2a0f8bf9fda28282c59e1db26db3730d6cab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce6132cdb3fa96f599f385750800b1b5373663d2fee48a3c63a8d979f66cc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e4c8297c01db11c191858fd6cf8a7511d64a9118a1c1c750d681e3841e7f3`  
		Size: 39.3 MB (39298708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce06b3288eb688faca7cdc69d231f81faaa16e369004bfaef06068b9687c27a`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 926.1 KB (926065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee6a894c26a477744c2bc2b3101e65176887db8b0aeb5cf047c5884101d455`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7451ade6546d4e3b9d7953419d27c746ce6b0e9f23a891197a416e9a34cf29`  
		Last Modified: Wed, 11 Dec 2024 20:31:24 GMT  
		Size: 701.9 MB (701874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90a5eb80de27a57eeff0fead5cf60c6a688e1e8ab5d0510560b51277ea74a`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e05105422fbe68ce9e63c322db62cb0c03c6d6ce8d543b5923087760b80230`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b19bb06f3c79a6921855e7577dfa4a8a2ee0dbfef49e3ef3d13eb64eb62ac6`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b714361da7137396fe322b09fc0e45fedcb305b31525630b48039fbf83e968c`  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dba9ba6eea486f48865f659aa8f43797dd9892579171a4220ee34e9c387d3`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02364dd300798b3a2cdffb4fd4c9996710276b95ddd51cd92bf0bdb976c03`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:e875371520bedaa2baffb1beeea80adefa9df8a91ab6f12b0f01cc032977ad47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8101bc5a78ebb73c600b37b58d257e800de5275e2f26524dff7688415b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5951a1e0fc56cf41e206b54e13f281427ce397d604402be27b44f6c0664377aa`  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:51890184c7f5923841b5d2667eaac8968a0bb450d93b8e377e98f09867f21012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742534627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37c525e8fa9c00cf8205958c87d66908faf2e0ddb4182a09a3a6dddce05f1a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584481da729d18de66076f7754e37c2bbc39cbf05bd725b8aa1ebf12e1429a`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 38.8 MB (38844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9437b11152e6789daaee1b8b2816829ecec5fe6f7b7e66d2b57cf0a8fb340f5`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 770.4 KB (770448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b80241375276135ce691e34844832bbc260efe1e17f69b3f6c0c63a909cf8`  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3461cd28120e1f6e3a2a5d1632a4c0b55c34c9f983e76358764a1c2ef23dd3`  
		Last Modified: Wed, 11 Dec 2024 20:35:36 GMT  
		Size: 675.6 MB (675556548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9a2303e4b89e2749df948d7b77b504b000b4b505078adcfb37a62dcd836a2`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacce055b74872fa011424cec1d27c67e1a1e63bd686fd81dc6f607572c5a6bf`  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a8748af089af62557555c76fee8ee17283476c34a1a2719fce6c853545f9a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fd38386fb9ec7054edc75e6910d24e7f2828b2898eba07f0ab18f31df677a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18f583723b3303d32822f4967c9220fefebebdca459e5cbccd3efd1a0b5a6f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c5cb759bf8528349b284da7a8f8e541fdda4bec66b63b16482c7eca1d329f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:38911045564e44eee162d11ab29804f5a2411172e6c55fc0959d3046d87c3e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d54da9ce17575a870692837ab8c7c5ee9b37c2595580d3efb48953b68c80e`

```dockerfile
```

-	Layers:
	-	`sha256:f05cbd60b6824e37fba0b063111378fdd30aa399b050e17cc9fbeb37de5ea28d`  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json
