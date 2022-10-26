## `couchbase:enterprise-6.6.5`

```console
$ docker pull couchbase@sha256:324b5fed9c7234ebe0dc9bfd36fa09c15cef5918c0137830f7d2fef4ac6bfca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:3647889b2777e4297b4749ae0083a97a51fd5a44b885d89b67db91673d4baf4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.9 MB (540906026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963f25a429eb63c59a94b76e4243e00d3b1cbf41c85283651b91d185c214fbe7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 15:57:13 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 25 Oct 2022 15:57:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 25 Oct 2022 15:57:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 15:57:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 25 Oct 2022 16:02:50 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Tue, 25 Oct 2022 16:02:50 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Tue, 25 Oct 2022 16:02:50 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Tue, 25 Oct 2022 16:02:50 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 25 Oct 2022 16:02:50 GMT
ARG CB_PACKAGE_NAME=couchbase-server
# Tue, 25 Oct 2022 16:02:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 25 Oct 2022 16:02:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 25 Oct 2022 16:03:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && dpkg --unpack ./$CB_PACKAGE     && sed -i -e '/Best heuristic/ a \ \ \ \ [ -d /run/systemd/system ] && return 1; return 0' /opt/couchbase/bin/install/systemd-ctl     && dpkg --configure couchbase-server     && apt-get install -yf     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 16:04:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 25 Oct 2022 16:04:01 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 25 Oct 2022 16:04:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 25 Oct 2022 16:04:02 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 25 Oct 2022 16:04:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 25 Oct 2022 16:04:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 25 Oct 2022 16:04:10 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 25 Oct 2022 16:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 16:04:10 GMT
CMD ["couchbase-server"]
# Tue, 25 Oct 2022 16:04:10 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 25 Oct 2022 16:04:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c363d586f4d6eee662a9e0f273458c615ad1280fafe8bdffd8aaf8bcce83e523`  
		Last Modified: Tue, 25 Oct 2022 16:05:58 GMT  
		Size: 6.2 MB (6232224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d631a277179bfc7873b2456b93f46899e261a4706b83270daac24b99242502`  
		Last Modified: Wed, 26 Oct 2022 16:53:28 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678f36ffb3a919177e52695c7da692fe6f6fa0bae1a0c4ffc2fd7cbb387025fb`  
		Last Modified: Wed, 26 Oct 2022 16:54:24 GMT  
		Size: 505.7 MB (505651889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832d661b079cad7a857432aca6f61ae9938bf1ca45a10f11b4f89cc9a3530c0`  
		Last Modified: Wed, 26 Oct 2022 16:53:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9da3d2038bf7d24d6db2b72cd37c48b53f16129433c70701ab8cbd64faa3c27`  
		Last Modified: Wed, 26 Oct 2022 16:53:28 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565ed7e513831cf52e213218621b8dca3e75b9821f5513b6fcaa1857b48013a0`  
		Last Modified: Wed, 26 Oct 2022 16:53:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e490bd044e51746c9aa1adf17c282097f3ced910676857211d8df91970b70a8d`  
		Last Modified: Wed, 26 Oct 2022 16:53:26 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65685e09c3ea2518bc6a7d041b5477528191ae4c9aba0bdd1b9e6d719df1091`  
		Last Modified: Wed, 26 Oct 2022 16:53:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da171d6e09e4a7a93dc409c616cbed5e5502ad361dcf1b9e8c88f571cd044b87`  
		Last Modified: Wed, 26 Oct 2022 16:53:26 GMT  
		Size: 439.7 KB (439705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5629f67d5f59eb846d1a8ed702947044ea1317e8b0e8bc7bcd01eaa0ed04b934`  
		Last Modified: Wed, 26 Oct 2022 16:53:26 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
