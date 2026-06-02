## `couchbase:enterprise-7.2.8`

```console
$ docker pull couchbase@sha256:f825eafc18c5b10ab97aee0d9b0d59ea740df57a619dd90de62e67b2e320a43f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.8` - linux; amd64

```console
$ docker pull couchbase@sha256:bdf042f6deecc94eb072fef9380f27b378e33a8142284fcc2e3bf39621dae3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.3 MB (701327435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aba956cf5696c3f5be74c3101d428401877df0dab8eaad83d78b2cdda1636e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:21 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 02 Jun 2026 08:11:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 02 Jun 2026 08:11:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jun 2026 08:11:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 02 Jun 2026 08:11:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 02 Jun 2026 08:11:45 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8
# Tue, 02 Jun 2026 08:11:45 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb
# Tue, 02 Jun 2026 08:11:45 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 02 Jun 2026 08:11:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 02 Jun 2026 08:13:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 02 Jun 2026 08:13:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=09e11da52bc7aac2ecd12c33b7983f72cddb33b247d837cc6f3590483c45ad1c            ;;          'amd64')            CB_SHA256=ce04775b8070a5c810060abd80db286aa050fe082eba6890ed387f730ebfea8a            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 02 Jun 2026 08:13:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 02 Jun 2026 08:13:56 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 02 Jun 2026 08:13:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 02 Jun 2026 08:13:56 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:13:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 02 Jun 2026 08:13:57 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 02 Jun 2026 08:13:57 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:13:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:13:57 GMT
CMD ["couchbase-server"]
# Tue, 02 Jun 2026 08:13:57 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 02 Jun 2026 08:13:57 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaca32218178701ce3e20f8b8703a7dd7aac6783e57d9196e793679dd905ea5`  
		Last Modified: Tue, 02 Jun 2026 08:13:00 GMT  
		Size: 43.8 MB (43837940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5a777e3658eaa36971dc10d02eaa660751aa8f0346cd47c3aab9e2c245d1ed`  
		Last Modified: Tue, 02 Jun 2026 08:12:58 GMT  
		Size: 877.8 KB (877806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b890cf469d496d7da8aa5b487921ec60e6e2ee6a755bd89708d51d80d345fbc`  
		Last Modified: Tue, 02 Jun 2026 08:14:47 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c463aea8c27168345d24be4b8b279d41fa851d67468831a2890ec3633e387966`  
		Last Modified: Tue, 02 Jun 2026 08:15:04 GMT  
		Size: 626.9 MB (626871897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f149f63487313b19ca8087d09450872be30d6e1827b7fb9dc579c693b02609`  
		Last Modified: Tue, 02 Jun 2026 08:14:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cf17f8cd198e6b41d9af56619048d5fda657315da5fb985ae4db00eba10303`  
		Last Modified: Tue, 02 Jun 2026 08:14:47 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3711d71ba9f4d252dc040644a7ef9f3462d31c5da971cf091eef9af107c5cccf`  
		Last Modified: Tue, 02 Jun 2026 08:14:48 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71f59ea8d941263be6a10ffa3aa8c663f86ddec6d3d97db0b4f6e13f770a1bc`  
		Last Modified: Tue, 02 Jun 2026 08:14:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926730454991ae15db461eed54f9ff7eb17048971055659c79bef00ade4d37db`  
		Last Modified: Tue, 02 Jun 2026 08:14:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0527168d28574aa3f833549966344a2f3e8fd264765855f694914a59eb0d89c`  
		Last Modified: Tue, 02 Jun 2026 08:14:50 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.8` - unknown; unknown

```console
$ docker pull couchbase@sha256:3bf3ee9456a6b93e1f69c39bcb49ff1b2ce9a5c0f77b0f0778be633af692c8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dbc8900b5326b9335987a9ed7c1094ef642aa394df656ffd2bdf93efb1b17a`

```dockerfile
```

-	Layers:
	-	`sha256:e3447a86424ec856c8cfa4f8d2b0151a75b31701ce0d7931066b2802b1ab31a3`  
		Last Modified: Tue, 02 Jun 2026 08:14:47 GMT  
		Size: 37.5 KB (37522 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.8` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:7a54b484c0e4b2562f81792da9d6a00d5a186089529024f2762b335a28d81fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676668715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41525f49fa53199002dc73abf7a8c8690da1f904623c0812d590447fb0d4534c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:52 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 02 Jun 2026 08:11:52 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 02 Jun 2026 08:11:52 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jun 2026 08:11:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 02 Jun 2026 08:12:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 02 Jun 2026 08:12:17 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8
# Tue, 02 Jun 2026 08:12:17 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb
# Tue, 02 Jun 2026 08:12:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 02 Jun 2026 08:12:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 02 Jun 2026 08:14:35 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=09e11da52bc7aac2ecd12c33b7983f72cddb33b247d837cc6f3590483c45ad1c            ;;          'amd64')            CB_SHA256=ce04775b8070a5c810060abd80db286aa050fe082eba6890ed387f730ebfea8a            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:15 GMT
CMD ["couchbase-server"]
# Tue, 02 Jun 2026 08:15:15 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 02 Jun 2026 08:15:15 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024183dcc3e0f10a305e41a737106c359673d27b1e566bea9a56d0626eab8b89`  
		Last Modified: Tue, 02 Jun 2026 08:14:13 GMT  
		Size: 43.7 MB (43657115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa14cc6c88d269c8ae0b4a95a8f4f9c8e37053b9bd802ee7f642fcb55e8ecf63`  
		Last Modified: Tue, 02 Jun 2026 08:14:11 GMT  
		Size: 764.7 KB (764686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865a2eb98f2be4f88fc07feff66abc714192d608a64196b0dda6e6d753cf4fbc`  
		Last Modified: Tue, 02 Jun 2026 08:15:58 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888258799bc5956a37749e59b85889c8556b8dba996beded41475c97f5ddcaf`  
		Last Modified: Tue, 02 Jun 2026 08:16:11 GMT  
		Size: 603.4 MB (603363521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e230716791cf0e0b42b235dd215c293e6d30432e52dfea7871093baabe92e224`  
		Last Modified: Tue, 02 Jun 2026 08:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377569219de8f012033431f9e49618ffefbf75c1f10929d796d36458397c097`  
		Last Modified: Tue, 02 Jun 2026 08:15:58 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c161a3e5e0c311bd45410d7452a4e8f9882299f7fe8535d4a1e1d06c72a4c95f`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47def1ce3b0a0f14a92fb790d578963e00b7186e1517c25655cd616559d0ba17`  
		Last Modified: Tue, 02 Jun 2026 08:15:59 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a08287637b3e65fcecb4edd6a1f69ce4e119587d2d08ef9182080e6a65b2dc`  
		Last Modified: Tue, 02 Jun 2026 08:16:00 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23ce90234f60532c935fb301bb94b0f9f6700921816f361707a237913c1d939`  
		Last Modified: Tue, 02 Jun 2026 08:16:00 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.8` - unknown; unknown

```console
$ docker pull couchbase@sha256:76fd938ef849fd46dbf495a5e407eef49aba0771aa3c4739f84b3434f9af2413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0477bdf319d371140080d873d122948f9a184003b95f32d67f29616978a7473d`

```dockerfile
```

-	Layers:
	-	`sha256:5e000be86dd0831f8c64ad9bc164c949b8f39ab0f12d3ab85d396066254283ef`  
		Last Modified: Tue, 02 Jun 2026 08:15:58 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json
