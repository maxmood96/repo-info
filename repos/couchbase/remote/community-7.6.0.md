## `couchbase:community-7.6.0`

```console
$ docker pull couchbase@sha256:b471a9b098fada3dabfa790fd2352bf2a3352e61d81f1704ec1c1393ac6370d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:d9303f5774991591d2e43be0c29c8336843d80ead245f60537f0ddab05045c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (389969555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a67e9ed5c343a77e278a38233cfa1463ec2db24d6020d4c6b42b6eb10f5a74d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Mar 2024 02:04:28 GMT
ARG RELEASE
# Mon, 25 Mar 2024 02:04:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Mar 2024 02:04:28 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Mar 2024 02:04:28 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 02:04:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 02:04:28 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Mar 2024 02:04:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aef9a97bcf6858ebb5e12663c0a120b83a4e65476117c3bce791fe3da12034`  
		Last Modified: Tue, 25 Mar 2025 18:26:44 GMT  
		Size: 6.2 MB (6196202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170629758d310c4aea7bcd43bfc2f2d423a402427e616fc497b1c4db23ced35`  
		Last Modified: Tue, 25 Mar 2025 18:26:44 GMT  
		Size: 6.4 MB (6448207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b703640f3f8349b5fb26a10ae4c0b2c655e6fafe50db014e28e797a9ef28a40`  
		Last Modified: Tue, 25 Mar 2025 18:26:44 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a0e5dbed8e85290080c08b94bb31f26dcbe15fbf089c0c4be5970fdd25f780`  
		Last Modified: Tue, 25 Mar 2025 18:26:50 GMT  
		Size: 349.8 MB (349809401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cceb6d1fb55f850436546c0ab5e0c77dbd43562a0e9ba9446cf95f984c01ae`  
		Last Modified: Tue, 25 Mar 2025 18:26:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007a724a5c420ca905df9bc7dc66b6d50dc22bb0887b4a5f3af334f856e9e6bf`  
		Last Modified: Tue, 25 Mar 2025 18:26:45 GMT  
		Size: 660.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe07186fc95c73a1159ab0b622555b6e29da5bb2f53ce43b1bc029a54862bb7`  
		Last Modified: Tue, 25 Mar 2025 18:26:45 GMT  
		Size: 693.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18376b7c98ce053a9bbe01abd434585e7f0f79d49f1edf3631b48d5aa810cf0d`  
		Last Modified: Tue, 25 Mar 2025 18:26:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7840e0bd1e6859a93a2021d591fde5a8290cba21783d2d9d6ad9f198b605f9b8`  
		Last Modified: Tue, 25 Mar 2025 18:26:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e493eb13e9d29c410904db719cdd773785d0937f4a6ce7456370fe711469c355`  
		Last Modified: Tue, 25 Mar 2025 18:26:46 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:4e20737b7df6eef1c62fc9216a783c3e51d04b6c0acce504673654f6e828347a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb06a972d3be604e2b1ad7c1b612f693d511bdab814455bd357642512c8f78df`

```dockerfile
```

-	Layers:
	-	`sha256:d022d22af14ff2efe84f2f459ce020d63c62b3011e9ec54e2fc07a48354fa96f`  
		Last Modified: Tue, 25 Mar 2025 18:26:44 GMT  
		Size: 35.5 KB (35452 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9f8c6a7cb78950499d2e702d6aaf4a36f3d449af538d60c973be8e3134aa1129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.7 MB (370736109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5772f22ca756798d92129d9de4fe13925f9e8c2c1d397078049cd692212faefd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Mar 2024 02:04:28 GMT
ARG RELEASE
# Mon, 25 Mar 2024 02:04:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Mar 2024 02:04:28 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Mar 2024 02:04:28 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 02:04:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 02:04:28 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Mar 2024 02:04:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979c8730a17e553b24586fbc924f24b64dd0f55ea6166c61ae5bb4cecbdba32e`  
		Last Modified: Tue, 25 Mar 2025 18:45:08 GMT  
		Size: 6.0 MB (6032171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c477633c69e0be7de472aaf5478e192e618fd269050e579983019bfaf5a0f2`  
		Last Modified: Tue, 25 Mar 2025 18:45:08 GMT  
		Size: 5.4 MB (5380088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc2b8374ff88b991c161d37a712ec426d2a9c02976d9f9f95d9159d62dcbe9`  
		Last Modified: Tue, 25 Mar 2025 18:45:08 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357ce473171790e7e09c6f9c189041122aed2af846f6254f7e4a1a7a76a8b14`  
		Last Modified: Tue, 25 Mar 2025 18:45:16 GMT  
		Size: 333.3 MB (333345337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eba42f27bf0973394405d90dd945080aba044895f4c46ea9a0525b5ffbcf7a`  
		Last Modified: Tue, 25 Mar 2025 18:45:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f57dccd10709d9fef4561975c816bd3ea7a593cfb26053b34c9c58d132fbb80`  
		Last Modified: Tue, 25 Mar 2025 18:45:10 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0492c8f8d3562a9b6d432e6824fda8d169c2ff784ea8ddbc8c8e7749e0c075ca`  
		Last Modified: Tue, 25 Mar 2025 18:45:10 GMT  
		Size: 692.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcf123c0f60bec1d2fd838de883113a95b9b423b296136f186b2ee704c3e22a`  
		Last Modified: Tue, 25 Mar 2025 18:45:10 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e00d625827dd9412959b23994676f4463b6c0dc02cd0c1ad17d867c997c7d2c`  
		Last Modified: Tue, 25 Mar 2025 18:45:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc0bfb242f87074db4e90ab4abaa504552d1412b683e73dde3d7dc8af846098`  
		Last Modified: Tue, 25 Mar 2025 18:45:11 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:278a37cc842276914ca514c0301d1d148a369ffcc2f239dc8a3e4d07cd0e62d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f7e835d19605289420d0f24f86f668cfe6b6afda3283e36229499a2928753f`

```dockerfile
```

-	Layers:
	-	`sha256:89d2616981612789f779cae161c746c0a175b627e4dc73b4a023be6ffcc9f5ae`  
		Last Modified: Tue, 25 Mar 2025 18:45:08 GMT  
		Size: 35.6 KB (35625 bytes)  
		MIME: application/vnd.in-toto+json
