## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:d5324b4c425fc1c93a0403bfee1d66e917816418dcf2054747e34091365983d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:b31353741b7b51d5f98f59c36c975cabd4c243e8c9d74554e955350847035199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **892.2 MB (892244974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2e2a11310aea56464c5c982fd2a1f9d2a7f2f549103688728492036fae3c8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 20:19:03 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 30 Mar 2026 20:19:03 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 30 Mar 2026 20:19:03 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 30 Mar 2026 20:19:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 30 Mar 2026 20:19:35 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 30 Mar 2026 20:19:35 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1
# Mon, 30 Mar 2026 20:19:35 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb
# Mon, 30 Mar 2026 20:19:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 30 Mar 2026 20:19:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 30 Mar 2026 20:19:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Mon, 30 Mar 2026 20:20:22 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=dba9dbeb2ff3928e62ebecf154353e1574e50e4e2548664ea25cb52bc2028cc7            ;;          'amd64')            CB_SHA256=194504d728e6725068a15a7e19e7b60685a3fe4c70394112e132805445174128            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 30 Mar 2026 20:20:22 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 30 Mar 2026 20:20:22 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 30 Mar 2026 20:20:22 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 30 Mar 2026 20:20:22 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 30 Mar 2026 20:20:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 30 Mar 2026 20:20:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 30 Mar 2026 20:20:23 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 20:20:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:20:23 GMT
CMD ["couchbase-server"]
# Mon, 30 Mar 2026 20:20:23 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 30 Mar 2026 20:20:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84a56e1fe4d30b126cb50e11701966a7ea25a06e09459873b18e0c5145cf08f`  
		Last Modified: Mon, 30 Mar 2026 20:21:27 GMT  
		Size: 45.9 MB (45948967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feef203e601851e3bb8a15182df83de7d692c67b00e0f61889e7613aa231a9f`  
		Last Modified: Mon, 30 Mar 2026 20:21:25 GMT  
		Size: 878.8 KB (878834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21ef29724d5c20f72800b498d932abaa0df47780c4ac57a6b2d4e6a1a9f01da`  
		Last Modified: Mon, 30 Mar 2026 20:21:25 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a29a965f5f7815bac4bdaf3a872d859665b3771720c0240e86a08e3ebd0a79`  
		Last Modified: Mon, 30 Mar 2026 20:21:42 GMT  
		Size: 815.7 MB (815678189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5229acdfa28078e9486468053c2f9f7508f0a1275461762ee57790d2ad3e2214`  
		Last Modified: Mon, 30 Mar 2026 20:21:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dabb802df4cea28d259348d49bfb7190ff55ba79eb9f231fb126890d0aaf60`  
		Last Modified: Mon, 30 Mar 2026 20:21:27 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db01d8026059331915c2386659d2715b0d756acf0a5825d3c8aa524171067acf`  
		Last Modified: Mon, 30 Mar 2026 20:21:28 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff41aa31fbb9f5b1071e0660eedb2d8d14139e08134365067f1b78091358d4d5`  
		Last Modified: Mon, 30 Mar 2026 20:21:28 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672117169e25fb5d48d10d9e8dd38b27f7d121a98711b4def7508b20f8429a9`  
		Last Modified: Mon, 30 Mar 2026 20:21:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3202499780ea5cfc7d93d499e3d7bc22ed3e4ef0d47f63201c361d666804b23a`  
		Last Modified: Mon, 30 Mar 2026 20:21:29 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:d28b21a827d62e0d639c044ee3adb8567bc142c50a14451bcb02a92ff95267dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b49c69080b32d40b8aebcd0dba4721f034da3d5be5c10afd76c78c5b1421080`

```dockerfile
```

-	Layers:
	-	`sha256:94675841e3809572cc893a6fc6495e6fea47471ea2825cf3cd452f39a549f38f`  
		Last Modified: Mon, 30 Mar 2026 20:21:25 GMT  
		Size: 38.1 KB (38137 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9fb96e6618dba39d9c22fb3d9f7120a3139f1ce547f276327865da5b97c149e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **849.0 MB (848983310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5f61ca6ebee0fead527b7db03503ddefb9721c99871d2819e0de44e67ad74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 20:18:58 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 30 Mar 2026 20:18:58 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 30 Mar 2026 20:18:58 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 30 Mar 2026 20:18:58 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 30 Mar 2026 20:19:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 30 Mar 2026 20:19:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1
# Mon, 30 Mar 2026 20:19:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb
# Mon, 30 Mar 2026 20:19:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 30 Mar 2026 20:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 30 Mar 2026 20:19:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=dba9dbeb2ff3928e62ebecf154353e1574e50e4e2548664ea25cb52bc2028cc7            ;;          'amd64')            CB_SHA256=194504d728e6725068a15a7e19e7b60685a3fe4c70394112e132805445174128            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-enterprise_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 20:20:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:20:14 GMT
CMD ["couchbase-server"]
# Mon, 30 Mar 2026 20:20:14 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 30 Mar 2026 20:20:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168bcf56bba2b9a39fdcfdb385316176c268f8c64dc19d0faffa15c25f5ac2f8`  
		Last Modified: Mon, 30 Mar 2026 20:21:16 GMT  
		Size: 45.8 MB (45839011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee88763c9ae35d12e11c07e90d5863cbeb868b0cfe97e26173bd07b76a481f8`  
		Last Modified: Mon, 30 Mar 2026 20:21:14 GMT  
		Size: 765.8 KB (765833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33cf07c36d60851202f2f2aae48b0e93aa36e577687209f69bde20d6c6a789`  
		Last Modified: Mon, 30 Mar 2026 20:21:14 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0c05fd4349ff8ded844399ce50860bc68e9b7a11fc709844057bbf2c1d0a9`  
		Last Modified: Mon, 30 Mar 2026 20:21:33 GMT  
		Size: 773.5 MB (773501769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac7867d5fe90921e4fd1d66327aad83c6fc1a883194d209b2c5dc3eb14bc00`  
		Last Modified: Mon, 30 Mar 2026 20:21:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7509bbe415cab46b50e2dec00450cebc6ab4efed944a8cec67567f677269d5fd`  
		Last Modified: Mon, 30 Mar 2026 20:21:16 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c78cfc3d449b04abc198c56a56de080e7b60436816875e409a322ddf41a70c`  
		Last Modified: Mon, 30 Mar 2026 20:21:17 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f007792bb353d9607ef3e438bf5c15e1a859c36dcbae4855f328b1fde55d5ce`  
		Last Modified: Mon, 30 Mar 2026 20:21:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3c738dcc243d7e0beb3be877a187f9da6f482f27699a4e0c87ad91a9bf1a32`  
		Last Modified: Mon, 30 Mar 2026 20:21:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0bf6dabead6ae57b3249bd2bfe69fc85ddfd65da124a4ca7271e0cef4f2b2d`  
		Last Modified: Mon, 30 Mar 2026 20:21:19 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:789ed176d0c1228e348c9d0eff334da26ec6d7bd8cc5ebeff0e9a847d9d472dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09657888038b1d0487e74f50fcd2dd603db2fb8489cb7769fae0d8f80ec7294`

```dockerfile
```

-	Layers:
	-	`sha256:a13fb9cf270c2928dcf80cb26668bb5b17132e3083b13c66b5bfe01d0532fe80`  
		Last Modified: Mon, 30 Mar 2026 20:21:14 GMT  
		Size: 38.3 KB (38347 bytes)  
		MIME: application/vnd.in-toto+json
