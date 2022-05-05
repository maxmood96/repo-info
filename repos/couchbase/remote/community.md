## `couchbase:community`

```console
$ docker pull couchbase@sha256:f16393a7a4fe42c0c1d8ec1f7ebb1236b5ce040fb20b1dd1df7982d5aa9a4522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:dcd5ea2ad956fd604fd72c5bbf5c6497fbff81b7c3124f087a4c405fa683794a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349036570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcf4768ea45dd63c3f9f6c42f881ba88ec7f27dca94e0c3c189b21bb265e42a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:04:47 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 30 Apr 2022 00:04:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 30 Apr 2022 00:04:48 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 30 Apr 2022 00:05:04 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 05 May 2022 01:19:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0
# Thu, 05 May 2022 01:20:51 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb
# Thu, 05 May 2022 01:20:51 GMT
ARG CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539
# Thu, 05 May 2022 01:20:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 05 May 2022 01:20:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 05 May 2022 01:21:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 05 May 2022 01:21:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 05 May 2022 01:21:37 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 05 May 2022 01:21:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 05 May 2022 01:21:38 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 05 May 2022 01:21:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 05 May 2022 01:21:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 05 May 2022 01:21:39 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 05 May 2022 01:21:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 May 2022 01:21:39 GMT
CMD ["couchbase-server"]
# Thu, 05 May 2022 01:21:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 05 May 2022 01:21:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76937b0923f63ef62ef0ce2435f73244f7f909cc74136aba1228f2e2574af748`  
		Last Modified: Sat, 30 Apr 2022 00:18:06 GMT  
		Size: 6.3 MB (6250617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b87a2b2a6196c22a78238112e5374a0313b7f12ffa81de4e20fb1b30a71910`  
		Last Modified: Thu, 05 May 2022 01:28:42 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b9f08d33261a60cf59570e2690951a901c4f4e0939266164b0122ac47c143a`  
		Last Modified: Thu, 05 May 2022 01:29:21 GMT  
		Size: 314.2 MB (314215352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27898e2d18af06c356de256d232598367b9b126906be6e751d03d6d69fd8b80e`  
		Last Modified: Thu, 05 May 2022 01:28:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7394672a0d82489fda5edcf3b881732ceb6fe5ce1e0a10ca495f2eb142b6d5`  
		Last Modified: Thu, 05 May 2022 01:28:39 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87707b3ad98436db937afa9407af8bd37ec8fd7e50ee24a7cc595cc08b6ab6f`  
		Last Modified: Thu, 05 May 2022 01:28:40 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74f6f2b92d5ca706920d5076fb3351f8669231c5523fd31ae98e3de6de3766`  
		Last Modified: Thu, 05 May 2022 01:28:39 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941c338efdaf95ec7eeef7950ca7c4085aef6c660799cd6e5f44d2c82acd7ea`  
		Last Modified: Thu, 05 May 2022 01:28:39 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97005019eda8e8d2e6655c02758c4104f478c0a3a5c1e69cbd43f4990a456f69`  
		Last Modified: Thu, 05 May 2022 01:28:40 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
