## `couchbase:enterprise-7.2.6`

```console
$ docker pull couchbase@sha256:792a927e3376c2fa33803ece5b69408275f59ddd0922b6f1e8ef4055f2451083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:742742c2b9462ff5228bd6b543c73a5228def3131c68084ee3ce57255ca480be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.7 MB (690668356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff663744ea006c54fb586c0520424611bf4d66992aae61c30c96aafe101ed29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:07:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:07:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:07:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6342502ed45c496fc9a772bf28dce27961b7f3f260815b8c9bc998c905ed0949`  
		Last Modified: Thu, 12 Jun 2025 22:54:37 GMT  
		Size: 44.5 MB (44462513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e119535dc9d9cd9b87bb7f9f480283d921f6e1fd9995f68a8df6b3dae2afdb`  
		Last Modified: Thu, 12 Jun 2025 22:54:32 GMT  
		Size: 877.9 KB (877888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8080ed5fe938e91c6fb2cf13df2c6774d671673dc21f86303370c6826fbfa0`  
		Last Modified: Thu, 12 Jun 2025 22:54:32 GMT  
		Size: 3.7 KB (3729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa01ec3e95beb8d8829a4ca55d4f1686ef293b72d9199314aa9ec1e972c4b1`  
		Last Modified: Thu, 12 Jun 2025 23:32:34 GMT  
		Size: 615.6 MB (615605698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3dc2fd94d56840efabe44416d9d3cd55577edf187a3534a96b66c0b1be9954`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463b5f2c01b7d56a91294b84e569e56c7bc8141e015416fecf9ea580f176884f`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fea10eaf0607de29318d5121d71e889e9bdb509e93e78f697e779b8a62ac8`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0341c875eca6c4eebc54ca023e7ae23dba967372aaad35d4cd97ade0f30f0b24`  
		Last Modified: Thu, 12 Jun 2025 22:58:09 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76f5055fc3ff068332267dfdcea771ce824827b8ac180e2b1f933eb706360d`  
		Last Modified: Thu, 12 Jun 2025 22:58:14 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9add43c4fae696f20ad685bd9ffc3306cbfcab18cd737b4aa91db3f2b37fce`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:9c299b47aca350a282338de4edf9aaf24f5c7b56250aca5fa2c704505db1081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6421b0be3156000fa4bb38046e52c19cbf71ed14181b771285ed0e77d7e5da`

```dockerfile
```

-	Layers:
	-	`sha256:fdd92a35fd8b2955a09e81f54efb29a1bef36480b164e39b65b7d54e11bacd15`  
		Last Modified: Thu, 12 Jun 2025 23:31:44 GMT  
		Size: 37.6 KB (37563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6c4ed7bb51e115b3bf6d8b468889f4d55a30f3276c98350ce947c0887413a98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.6 MB (665628710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3423fe1f383e5d0cba733bc1312febe19a49580cbf612ba972d7e2858bdcfcf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 12 Jun 2025 11:07:10 GMT
ARG RELEASE
# Thu, 12 Jun 2025 11:07:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 12 Jun 2025 11:07:10 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:07:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:07:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:07:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a666f0d75a91d1bdd972442dfd700631ae19f600aec32195844e217e853e94`  
		Last Modified: Wed, 02 Jul 2025 04:40:27 GMT  
		Size: 43.6 MB (43614791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340f0f0e8d481479063852b8f2a2deb3fb25af94716cb5f2ee3520b7b59e1f9`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 764.6 KB (764615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a52d1b88c6baeae22357585596bb42f9982b8230a7efad6fa85a688a164eb`  
		Last Modified: Wed, 02 Jul 2025 04:51:42 GMT  
		Size: 3.7 KB (3728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98b140b3d4f89045ab423bf9dfd4f56a75cad590b140b17894ed14a294f8e87`  
		Last Modified: Wed, 02 Jul 2025 05:32:04 GMT  
		Size: 592.4 MB (592386367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6a6850f8de764878269de154466490357a74227ac526720f66af9bba719457`  
		Last Modified: Wed, 02 Jul 2025 04:51:42 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515701c6e702222ded07de8a894674e7d5d5a35e93665aadd61188311fca1323`  
		Last Modified: Wed, 02 Jul 2025 04:51:43 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e178ace3d0e1fb9bc7079b1d7b96cdd912deb8aecf26fdd653590aa7fec16af`  
		Last Modified: Wed, 02 Jul 2025 04:51:43 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f35e3c92e046741760d994d467540c2d616afd3c8ee0c07f8e375028eb96c66`  
		Last Modified: Wed, 02 Jul 2025 04:51:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225042103265e293c8d46a7826c7931395d7bf6f3f150b67544c1508ffb14074`  
		Last Modified: Wed, 02 Jul 2025 04:51:42 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4848dfbe14cea7d2030cd20b0f680ed7f523e208816415c0270b28da1f0359`  
		Last Modified: Wed, 02 Jul 2025 04:51:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:10768e9be5091508492103323e1266628d24db5c368fb5d7c8723f5d86b00cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4d59765c9ed526bc5090c2412de2331d75ab8e72f261ae4f70d7ea1b6e5111`

```dockerfile
```

-	Layers:
	-	`sha256:0967c01645b5f57bfb9a99497fa95078fd42ced229169920df3770a0d24218b6`  
		Last Modified: Wed, 02 Jul 2025 05:31:44 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json
