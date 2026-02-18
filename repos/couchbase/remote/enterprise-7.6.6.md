## `couchbase:enterprise-7.6.6`

```console
$ docker pull couchbase@sha256:1fe8beea777966ebe9acf255a934e3aada501f9db1875e8e3c4e7f992935dd46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.6` - linux; amd64

```console
$ docker pull couchbase@sha256:8d161706ae2094e13562299d4fd160e515ebb0582f4b92e83fcf8b0829f8f5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.8 MB (794752824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba6d2334b1653978bf9a95f862ea981c9273d5f972c76d43d7a9c0a4177e675`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:22 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:13:22 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:13:22 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:13:22 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:13:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:13:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 17 Feb 2026 20:13:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:13:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:13:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:13:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Feb 2026 20:15:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:15:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:15:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:15:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:15:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:15:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:15:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:15:03 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:15:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:15:03 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:15:03 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:15:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4466cd6c55dc49e9e55b0fb542576ad6a61145742b7bbfad61e0cfa2e034fc3`  
		Last Modified: Tue, 17 Feb 2026 20:15:57 GMT  
		Size: 39.3 MB (39303070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c8c8d52f9de51e9ceae1fbc27c73d098360b3370caef703b4a412cd10d5709`  
		Last Modified: Tue, 17 Feb 2026 20:15:55 GMT  
		Size: 926.8 KB (926773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71703a05f72e767ba6626b15b3926244615cf2934c907a7231086762cba35138`  
		Last Modified: Tue, 17 Feb 2026 20:15:55 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c29e8234117c78403dd7a3bd0a30bd4494a82302b7ad93089d960e03c1e6dc`  
		Last Modified: Tue, 17 Feb 2026 20:16:13 GMT  
		Size: 725.0 MB (724980432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78202e06bc96ddc7db99f3c6e85a2ee1da7eac4799b1b91ad52eb83554d4ef5c`  
		Last Modified: Tue, 17 Feb 2026 20:15:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b6d84150494aef37669255ae498501c1b83cc6e1b663ef4589f29f71e5991f`  
		Last Modified: Tue, 17 Feb 2026 20:15:56 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a42d38a7b9ef0d0a798cc585b432ca6be976a1dbbba627ffea6328886940db4`  
		Last Modified: Tue, 17 Feb 2026 20:15:57 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103cd14afd859ed1031d10b8575b8241f74aba6909296d34db2b9086213c25f9`  
		Last Modified: Tue, 17 Feb 2026 20:15:57 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598f7d599891d226a68eb7a96fff27260b7d8a12b33d81134db41d576d0de882`  
		Last Modified: Tue, 17 Feb 2026 20:15:58 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b29e2d3eae3e218651e6c284e01324eedc3cdb0dc2383078d5042d0447581`  
		Last Modified: Tue, 17 Feb 2026 20:15:59 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:71406886ffe5f92e6fc70baf3cf83557a35a27f754a664efda9e3996e6ceb120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c53514a1c28596c0a24c96bf524e4834d7cba5f0e81a03f6acc52fb42a8ed20`

```dockerfile
```

-	Layers:
	-	`sha256:0ed8a874d79f93343b5e870c5d48f0e8e654b096670384f8f4321fdf4b6ca83d`  
		Last Modified: Tue, 17 Feb 2026 20:15:55 GMT  
		Size: 35.8 KB (35773 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:53606f129b2b01f25329ec3fd413c33c6786ba336f31867cce8187275d0da1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.5 MB (763460016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99da2fd392a87410fc8a7beaaab30a2bf4d2208ff717532cb4be2c2e2a80e088`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:43 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:12:43 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:12:43 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:13:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:13:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 17 Feb 2026 20:13:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:13:11 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:13:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:13:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:14:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:14:16 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:14:16 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:14:16 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:14:16 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122f69c4b77a668f86c3934c1791dba49743ed787589b4f02e53d694613241b7`  
		Last Modified: Tue, 17 Feb 2026 20:15:08 GMT  
		Size: 38.9 MB (38867503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6a0c9a241bc3601fad59b4e69ec377b30680e772f32c8a362f7fbcc97b6b14`  
		Last Modified: Tue, 17 Feb 2026 20:15:06 GMT  
		Size: 775.4 KB (775357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c56edb8a63c20f3bb6054253d2ed11619f5b5e220300d0403810386249db6a`  
		Last Modified: Tue, 17 Feb 2026 20:15:06 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced0cc3be39c7464c36b65549e80b65cc5abae159d3c119c72c054a3dd8d75d2`  
		Last Modified: Tue, 17 Feb 2026 20:15:19 GMT  
		Size: 696.4 MB (696427031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a572c15e15612998be2e733abdc7c5418076c81d49e6931edfe2421fc3656b4`  
		Last Modified: Tue, 17 Feb 2026 20:15:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cef52513fda0c39bada5f6f751ba4882a5782d6c64c51609f53d1da2324f5f1`  
		Last Modified: Tue, 17 Feb 2026 20:15:08 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415d9f0d5aa7beb68f48fc73223addce39c1678dff2c8ec0081082a9c42bc5e`  
		Last Modified: Tue, 17 Feb 2026 20:15:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c338756f8a1170dff38726d97435dceb3430034d716a3244fc649f98ff1edf`  
		Last Modified: Tue, 17 Feb 2026 20:15:09 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdd641dcd783ffea8bf52fe1cca09583c718cd20cd6844be80a403bbeb0b9d5`  
		Last Modified: Tue, 17 Feb 2026 20:15:10 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab4bccf6faf0d9cb3ae9386383127e7ffbdd0f947cf049cf01b56cfc54f8b71`  
		Last Modified: Tue, 17 Feb 2026 20:15:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:7c12d8b0b28f9b70c9e117ad69c0f4bd6d08dbfcc165a81f8ff2c9f872403645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916441890dd7a86275ce70dc095ebc5bbbc11a9730ad3400e22a449fa3a380f7`

```dockerfile
```

-	Layers:
	-	`sha256:c8085e344242896d25c9702e68eb984a724685228b60040d677e900fbcee1539`  
		Last Modified: Tue, 17 Feb 2026 20:15:06 GMT  
		Size: 36.0 KB (35957 bytes)  
		MIME: application/vnd.in-toto+json
