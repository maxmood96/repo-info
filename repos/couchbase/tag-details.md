<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.6.5`](#couchbase665)
-	[`couchbase:7.0.3`](#couchbase703)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.6.5`](#couchbaseenterprise-665)
-	[`couchbase:enterprise-7.0.3`](#couchbaseenterprise-703)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:3e3478fa598d7bc0351ff3f871a3729f170e203cae2537d82b1238f8f2c32115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:f72ec5368e7717090738ee8482e3b7f789081dc05ed626bbd943336ce9f6c5a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466123404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3ba9344525d4df833cddd277a6be68a3378380c280741cfaa4b59e3e3ae133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:32 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:18:25 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:18:26 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_VERSION=6.0.5
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Thu, 03 Mar 2022 21:18:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:18:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:19:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:19:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:19:27 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:19:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:19:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:19:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:19:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 03 Mar 2022 21:19:29 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 03 Mar 2022 21:19:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:19:29 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:19:29 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:19:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38c87d86f210f25cf76575efe9c2a7fb667b64e1429ac575da13cc8480eaaca`  
		Last Modified: Thu, 03 Mar 2022 21:22:34 GMT  
		Size: 15.9 MB (15922331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6028c9420ca2757fbbe2b27064d06198ce58596be407e810b37233076543524c`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a984d25823624d86044e66cf25b751e7aeb990eaa7961726a54da144460e92b`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e51405763846a3c533a2103497d025be3ed6973234f11e8835176b6ac5d338`  
		Last Modified: Thu, 03 Mar 2022 21:23:10 GMT  
		Size: 423.4 MB (423362699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b5ad04c42d581cbf6e11c1e389cc58f4bff4cdde919bf446f0e2322f43c4c5`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b47b1bdbf4466b7daf481100ab56cfd46373ff9c1ac9f90f262e710ad9a4c2`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4920893eb0531f9f4c43e73f4e6469614854ff4f7e0933597e7109a33ef57d`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af760a291be9f297b6b9643c22a36b32f33f21855dee68e65a679763433fa4b6`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae1b863d58282c72a5c0b8294fdd2e5ab25c18f27117ed246f037291bcbed37`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef14ecf10d36203553c4b36d466c8096384e9dd2a7270a6d0a47fc6fd55be81`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 125.6 KB (125559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7156c56b98703b8a249c5b4ab0fbc228ee82390ee09f9e78a8207967d4f44bd`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.6.5`

```console
$ docker pull couchbase@sha256:3886eb23092c8e42c9113ae8b3c2913be8e323130a958739c783bc3e3cd7e9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:02a08c0d00ee19dac6652145fd6f6afbb243fef8b4edea071ed39c99f68f0495
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.2 MB (541151121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7bffdfe1ce5fd50c58e005901ba305dd06b5da3993bae9f5913eb9aea1ddd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:46:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 02 Feb 2022 02:46:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:46:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_VERSION=6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:46:47 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Wed, 02 Feb 2022 02:46:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:46:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:47:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:47:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:47:50 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:47:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:47:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:47:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:47:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 02 Feb 2022 02:47:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:48:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:48:00 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:48:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:48:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1754ce27a7ccb86d31d56d18a4e72ba9d67be285a916c8bd17248b727560a47d`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 6.3 MB (6252084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f7756f763ab2246a969908f94fa0b42406e43c41ad14c419d0ad54beb50d9`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc09136fe05f40c619d016d0bba8dd53e94b083e1744226711ea3057fa8379`  
		Last Modified: Wed, 02 Feb 2022 02:55:16 GMT  
		Size: 505.9 MB (505890801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8fd0fde82ac5cd771ba6993145c59631f0e463809c2b727bd0056ad5f63665`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8719c5cb0fb42529c032006f2414cd51e3ae277a9a9e8e322c4fd2f5d92e80`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad063a0ccee34a72b08b383b143fd7c7f0069884c8a984966f56a6bd38c51f3d`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ec1e07f8149650f4c98a98a9259281d8fe9725da7995f86c9f57a58ec8dee`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdb27013dd5b6ec10d9b8b8778d61a0573b2146537c7a716824bde5f3650be4`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151da713f459104635e6d2bee7174258be998280138a69ec849ad19260f6129`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 439.8 KB (439771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fbf1915f342936bd4612edd42a845a199ff81e6bea379983490571b46ef6fd`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.3`

```console
$ docker pull couchbase@sha256:a9107d30b94e72ae515c1b9ee6c4ce103aff672cd92384dfd6d6e0905400da30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:eee6dbdb3392b1a15ac3aa80e5b52dd02c3ea047636f691bb55e00f0fea013ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653563052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3105d6fe843cbfe7245b49892b646e57fce588518a8cbca774ec04f3823f79a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:09:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Mar 2022 21:09:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:09:32 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f
# Thu, 03 Mar 2022 21:09:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:09:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:10:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:10:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:10:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Mar 2022 21:10:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Mar 2022 21:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:10:59 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:11:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:11:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97427f848e2d9332c4f8c5551ae43e02cdf7bcfa04dbcf30a06d1cc6a4c49fd`  
		Last Modified: Thu, 03 Mar 2022 21:19:56 GMT  
		Size: 6.3 MB (6252169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f42075137218fae5aca9743307b7b7d10824fbad3fd18e1532c96307e6365f`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e3774ef15da21a43788b1069fb301cf3ca4fb5f78ad0a3094dd447a5b8827e`  
		Last Modified: Thu, 03 Mar 2022 21:21:05 GMT  
		Size: 618.3 MB (618297366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc6621695b9dccc8bcacc41f39d1d7f33103c328c1bdbcb1d2a233e569f989`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a86041ec41dc4c14ee81bfedf0ea5fc0ad9dd5e6eab1070e8eb571fa7a854`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9154abf886fbbb562195401d129221f9eb7f3397931ae92112d31ce7f3f517`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec7977f99aa048a3f93646aa6e6d3419912edc03cb19ad31728f5aaaaa0f93`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3569b925f1a157f6cb0fbd214745d70c392aa5377cd5a84b1094e9d48a28f1e`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa8850bbbb4a3e7ea594ef4d720b92a8b5e4b2432b8621bd13498a2de32a91c`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 443.4 KB (443405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517bc00bb190b33d145488299238da1a6c4b3a3d6819bb8e145141d9f299cfb`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:d8647cc33ef20d722aa4846b20a0b9b4522938c21f983853bcb38cb7eb9cd84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:5a67921528a14ad2bf359440c7af1a3aabff9e7242f4cc637b0a0df39cc0c0b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429022348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504331a6b437867eb362445bc1d35f4c341aa5bf5f9e2c4840ca9060411b5403`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:11:15 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:11:16 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_VERSION=7.0.2
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Thu, 03 Mar 2022 21:11:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:11:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:12:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:12:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:12:14 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:12:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:12:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:12:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:12:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 03 Mar 2022 21:12:15 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 03 Mar 2022 21:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:12:16 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:12:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:12:16 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9228e5742f1a596a58835b57217984fb6cde7473b0f6e80fc6c369d17b79901`  
		Last Modified: Thu, 03 Mar 2022 21:21:29 GMT  
		Size: 6.3 MB (6261146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fe12d71ac6230ed642d7c1d5e132e4dfc5556bd9a170a44f4e76ea3f765cee`  
		Last Modified: Thu, 03 Mar 2022 21:21:26 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bfe17046bd421b9011d0b5ec9ab0df901abbff702ca715d11626705f8058ad`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1800c5ceadc33d1540a2f2eb4f85f8a8cca43b03e3b32b7ce3ccf611e322de2`  
		Last Modified: Thu, 03 Mar 2022 21:22:15 GMT  
		Size: 394.1 MB (394061464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afc4a7360a5e5bf71d09f84e3c1e5133067f509a0c9c7061a0a319a5d88aae3`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe943b6095d5a944e66aaf5778f6cad160c6007ce8a80a26be4fcb79c6c63d1`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f2b70cef4100b5fa0080abc1c3483a689a9294178d08a57e48ef8222f7c1b4`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c50463e751abf4722b32670ea320dc918d9135b7c129191a1cb8d3a907238`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1206ec5d85a9a15f8e9f3a3ccafa13b5afe2bc5ac4c289269af75df013bed8bd`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125e514453eab7e9f445e4b7f3cd295d8c1714b91d8383ae5608fe851e618b1`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 129.5 KB (129504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c9b415de2f0faf0fa560913db895750b0c37b7e69815ba217c735746a03807`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:fdd1d32c15ba32f2ede75472b17d2d46faa091b2dda3e7a332f985cdcc90162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:d201c08a35d3c387891b7db0f9b738729f3ca699c1e78bd3cffc97053314dc97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc22a56175d8ceef0a6c9b673b56e89cfacb9872a41898a14e8cad76c3f1e9c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:48:15 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:48:45 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:48:46 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 02 Feb 2022 02:48:46 GMT
ARG CB_VERSION=6.6.0
# Wed, 02 Feb 2022 02:48:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Wed, 02 Feb 2022 02:48:47 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Wed, 02 Feb 2022 02:48:47 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Wed, 02 Feb 2022 02:48:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:48:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:49:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:49:35 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:49:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:49:37 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:49:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:49:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 02 Feb 2022 02:49:38 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 02 Feb 2022 02:49:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:49:39 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:49:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:49:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e425b875a003fc3d1cb0261376c6c7b06f317ab62edc525973f364a81fa715b6`  
		Last Modified: Wed, 02 Feb 2022 02:55:33 GMT  
		Size: 7.4 MB (7369685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3acdc189fe79683161c15fb20351332b6fa980f57cbbf2c14f9bc7a91839b1`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d4566df698875020ff56135b7c4b9ccec4f3ed1ac3bf3647dbe9236e6e44d`  
		Last Modified: Wed, 02 Feb 2022 02:55:30 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a90fe8027662b5c454b3410922cf215003675074534f975f0fc8bfe298e55b`  
		Last Modified: Wed, 02 Feb 2022 02:56:08 GMT  
		Size: 320.0 MB (320018322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181984dfb9361c67df2c5b5993c6cc4f3b6065bfcbf12064a6661a56f279da5`  
		Last Modified: Wed, 02 Feb 2022 02:55:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9dbdaf5435709bc5339630f695ff46a9380d7db3b17b9042c96d3e027fd13a`  
		Last Modified: Wed, 02 Feb 2022 02:55:29 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53a24c87a7220452e0949585ac9559d60825e6ef9e70e29411569fc08e95e2e`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677095b029f2d6edf084c96e7c2cfa782c4450b6afa0fd39e253e8e0d62b2baf`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebc26fc42224cfbda435889d30e771ad96c02654c19e9fc3beb0e7f2eba22fe`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aefcba46347e465d160a8620560e12acac13b728cfbb45fadb512c02ce03d94`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 118.2 KB (118189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f556ceef96e57756240bf0d787fb91e7436f7630832ebb86197ffff68c7f143e`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:d8647cc33ef20d722aa4846b20a0b9b4522938c21f983853bcb38cb7eb9cd84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:5a67921528a14ad2bf359440c7af1a3aabff9e7242f4cc637b0a0df39cc0c0b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429022348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504331a6b437867eb362445bc1d35f4c341aa5bf5f9e2c4840ca9060411b5403`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:11:15 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:11:16 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_VERSION=7.0.2
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Thu, 03 Mar 2022 21:11:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:11:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:12:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:12:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:12:14 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:12:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:12:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:12:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:12:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 03 Mar 2022 21:12:15 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 03 Mar 2022 21:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:12:16 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:12:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:12:16 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9228e5742f1a596a58835b57217984fb6cde7473b0f6e80fc6c369d17b79901`  
		Last Modified: Thu, 03 Mar 2022 21:21:29 GMT  
		Size: 6.3 MB (6261146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fe12d71ac6230ed642d7c1d5e132e4dfc5556bd9a170a44f4e76ea3f765cee`  
		Last Modified: Thu, 03 Mar 2022 21:21:26 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bfe17046bd421b9011d0b5ec9ab0df901abbff702ca715d11626705f8058ad`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1800c5ceadc33d1540a2f2eb4f85f8a8cca43b03e3b32b7ce3ccf611e322de2`  
		Last Modified: Thu, 03 Mar 2022 21:22:15 GMT  
		Size: 394.1 MB (394061464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afc4a7360a5e5bf71d09f84e3c1e5133067f509a0c9c7061a0a319a5d88aae3`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe943b6095d5a944e66aaf5778f6cad160c6007ce8a80a26be4fcb79c6c63d1`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f2b70cef4100b5fa0080abc1c3483a689a9294178d08a57e48ef8222f7c1b4`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c50463e751abf4722b32670ea320dc918d9135b7c129191a1cb8d3a907238`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1206ec5d85a9a15f8e9f3a3ccafa13b5afe2bc5ac4c289269af75df013bed8bd`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125e514453eab7e9f445e4b7f3cd295d8c1714b91d8383ae5608fe851e618b1`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 129.5 KB (129504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c9b415de2f0faf0fa560913db895750b0c37b7e69815ba217c735746a03807`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:a9107d30b94e72ae515c1b9ee6c4ce103aff672cd92384dfd6d6e0905400da30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:eee6dbdb3392b1a15ac3aa80e5b52dd02c3ea047636f691bb55e00f0fea013ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653563052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3105d6fe843cbfe7245b49892b646e57fce588518a8cbca774ec04f3823f79a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:09:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Mar 2022 21:09:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:09:32 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f
# Thu, 03 Mar 2022 21:09:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:09:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:10:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:10:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:10:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Mar 2022 21:10:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Mar 2022 21:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:10:59 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:11:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:11:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97427f848e2d9332c4f8c5551ae43e02cdf7bcfa04dbcf30a06d1cc6a4c49fd`  
		Last Modified: Thu, 03 Mar 2022 21:19:56 GMT  
		Size: 6.3 MB (6252169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f42075137218fae5aca9743307b7b7d10824fbad3fd18e1532c96307e6365f`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e3774ef15da21a43788b1069fb301cf3ca4fb5f78ad0a3094dd447a5b8827e`  
		Last Modified: Thu, 03 Mar 2022 21:21:05 GMT  
		Size: 618.3 MB (618297366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc6621695b9dccc8bcacc41f39d1d7f33103c328c1bdbcb1d2a233e569f989`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a86041ec41dc4c14ee81bfedf0ea5fc0ad9dd5e6eab1070e8eb571fa7a854`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9154abf886fbbb562195401d129221f9eb7f3397931ae92112d31ce7f3f517`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec7977f99aa048a3f93646aa6e6d3419912edc03cb19ad31728f5aaaaa0f93`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3569b925f1a157f6cb0fbd214745d70c392aa5377cd5a84b1094e9d48a28f1e`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa8850bbbb4a3e7ea594ef4d720b92a8b5e4b2432b8621bd13498a2de32a91c`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 443.4 KB (443405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517bc00bb190b33d145488299238da1a6c4b3a3d6819bb8e145141d9f299cfb`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:3e3478fa598d7bc0351ff3f871a3729f170e203cae2537d82b1238f8f2c32115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:f72ec5368e7717090738ee8482e3b7f789081dc05ed626bbd943336ce9f6c5a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466123404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3ba9344525d4df833cddd277a6be68a3378380c280741cfaa4b59e3e3ae133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:32 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:18:25 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:18:26 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_VERSION=6.0.5
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Thu, 03 Mar 2022 21:18:26 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Thu, 03 Mar 2022 21:18:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:18:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:19:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:19:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:19:27 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:19:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:19:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:19:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:19:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 03 Mar 2022 21:19:29 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 03 Mar 2022 21:19:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:19:29 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:19:29 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:19:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38c87d86f210f25cf76575efe9c2a7fb667b64e1429ac575da13cc8480eaaca`  
		Last Modified: Thu, 03 Mar 2022 21:22:34 GMT  
		Size: 15.9 MB (15922331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6028c9420ca2757fbbe2b27064d06198ce58596be407e810b37233076543524c`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a984d25823624d86044e66cf25b751e7aeb990eaa7961726a54da144460e92b`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e51405763846a3c533a2103497d025be3ed6973234f11e8835176b6ac5d338`  
		Last Modified: Thu, 03 Mar 2022 21:23:10 GMT  
		Size: 423.4 MB (423362699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b5ad04c42d581cbf6e11c1e389cc58f4bff4cdde919bf446f0e2322f43c4c5`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b47b1bdbf4466b7daf481100ab56cfd46373ff9c1ac9f90f262e710ad9a4c2`  
		Last Modified: Thu, 03 Mar 2022 21:22:28 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4920893eb0531f9f4c43e73f4e6469614854ff4f7e0933597e7109a33ef57d`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af760a291be9f297b6b9643c22a36b32f33f21855dee68e65a679763433fa4b6`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae1b863d58282c72a5c0b8294fdd2e5ab25c18f27117ed246f037291bcbed37`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef14ecf10d36203553c4b36d466c8096384e9dd2a7270a6d0a47fc6fd55be81`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 125.6 KB (125559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7156c56b98703b8a249c5b4ab0fbc228ee82390ee09f9e78a8207967d4f44bd`  
		Last Modified: Thu, 03 Mar 2022 21:22:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.6.5`

```console
$ docker pull couchbase@sha256:3886eb23092c8e42c9113ae8b3c2913be8e323130a958739c783bc3e3cd7e9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:02a08c0d00ee19dac6652145fd6f6afbb243fef8b4edea071ed39c99f68f0495
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.2 MB (541151121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7bffdfe1ce5fd50c58e005901ba305dd06b5da3993bae9f5913eb9aea1ddd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:46:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 02 Feb 2022 02:46:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:46:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_VERSION=6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:46:47 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Wed, 02 Feb 2022 02:46:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:46:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:47:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:47:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:47:50 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:47:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:47:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:47:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:47:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 02 Feb 2022 02:47:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:48:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:48:00 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:48:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:48:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1754ce27a7ccb86d31d56d18a4e72ba9d67be285a916c8bd17248b727560a47d`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 6.3 MB (6252084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f7756f763ab2246a969908f94fa0b42406e43c41ad14c419d0ad54beb50d9`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc09136fe05f40c619d016d0bba8dd53e94b083e1744226711ea3057fa8379`  
		Last Modified: Wed, 02 Feb 2022 02:55:16 GMT  
		Size: 505.9 MB (505890801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8fd0fde82ac5cd771ba6993145c59631f0e463809c2b727bd0056ad5f63665`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8719c5cb0fb42529c032006f2414cd51e3ae277a9a9e8e322c4fd2f5d92e80`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad063a0ccee34a72b08b383b143fd7c7f0069884c8a984966f56a6bd38c51f3d`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ec1e07f8149650f4c98a98a9259281d8fe9725da7995f86c9f57a58ec8dee`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdb27013dd5b6ec10d9b8b8778d61a0573b2146537c7a716824bde5f3650be4`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151da713f459104635e6d2bee7174258be998280138a69ec849ad19260f6129`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 439.8 KB (439771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fbf1915f342936bd4612edd42a845a199ff81e6bea379983490571b46ef6fd`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.3`

```console
$ docker pull couchbase@sha256:a9107d30b94e72ae515c1b9ee6c4ce103aff672cd92384dfd6d6e0905400da30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:eee6dbdb3392b1a15ac3aa80e5b52dd02c3ea047636f691bb55e00f0fea013ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653563052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3105d6fe843cbfe7245b49892b646e57fce588518a8cbca774ec04f3823f79a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:09:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Mar 2022 21:09:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:09:32 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f
# Thu, 03 Mar 2022 21:09:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:09:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:10:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:10:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:10:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Mar 2022 21:10:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Mar 2022 21:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:10:59 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:11:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:11:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97427f848e2d9332c4f8c5551ae43e02cdf7bcfa04dbcf30a06d1cc6a4c49fd`  
		Last Modified: Thu, 03 Mar 2022 21:19:56 GMT  
		Size: 6.3 MB (6252169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f42075137218fae5aca9743307b7b7d10824fbad3fd18e1532c96307e6365f`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e3774ef15da21a43788b1069fb301cf3ca4fb5f78ad0a3094dd447a5b8827e`  
		Last Modified: Thu, 03 Mar 2022 21:21:05 GMT  
		Size: 618.3 MB (618297366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc6621695b9dccc8bcacc41f39d1d7f33103c328c1bdbcb1d2a233e569f989`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a86041ec41dc4c14ee81bfedf0ea5fc0ad9dd5e6eab1070e8eb571fa7a854`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9154abf886fbbb562195401d129221f9eb7f3397931ae92112d31ce7f3f517`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec7977f99aa048a3f93646aa6e6d3419912edc03cb19ad31728f5aaaaa0f93`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3569b925f1a157f6cb0fbd214745d70c392aa5377cd5a84b1094e9d48a28f1e`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa8850bbbb4a3e7ea594ef4d720b92a8b5e4b2432b8621bd13498a2de32a91c`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 443.4 KB (443405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517bc00bb190b33d145488299238da1a6c4b3a3d6819bb8e145141d9f299cfb`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:a9107d30b94e72ae515c1b9ee6c4ce103aff672cd92384dfd6d6e0905400da30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:eee6dbdb3392b1a15ac3aa80e5b52dd02c3ea047636f691bb55e00f0fea013ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653563052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3105d6fe843cbfe7245b49892b646e57fce588518a8cbca774ec04f3823f79a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:09:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Mar 2022 21:09:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:09:32 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:09:32 GMT
ARG CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f
# Thu, 03 Mar 2022 21:09:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:09:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:10:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:10:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:10:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:10:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:10:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Mar 2022 21:10:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Mar 2022 21:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:10:59 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:11:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:11:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97427f848e2d9332c4f8c5551ae43e02cdf7bcfa04dbcf30a06d1cc6a4c49fd`  
		Last Modified: Thu, 03 Mar 2022 21:19:56 GMT  
		Size: 6.3 MB (6252169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f42075137218fae5aca9743307b7b7d10824fbad3fd18e1532c96307e6365f`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e3774ef15da21a43788b1069fb301cf3ca4fb5f78ad0a3094dd447a5b8827e`  
		Last Modified: Thu, 03 Mar 2022 21:21:05 GMT  
		Size: 618.3 MB (618297366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc6621695b9dccc8bcacc41f39d1d7f33103c328c1bdbcb1d2a233e569f989`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408a86041ec41dc4c14ee81bfedf0ea5fc0ad9dd5e6eab1070e8eb571fa7a854`  
		Last Modified: Thu, 03 Mar 2022 21:19:54 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9154abf886fbbb562195401d129221f9eb7f3397931ae92112d31ce7f3f517`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec7977f99aa048a3f93646aa6e6d3419912edc03cb19ad31728f5aaaaa0f93`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3569b925f1a157f6cb0fbd214745d70c392aa5377cd5a84b1094e9d48a28f1e`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa8850bbbb4a3e7ea594ef4d720b92a8b5e4b2432b8621bd13498a2de32a91c`  
		Last Modified: Thu, 03 Mar 2022 21:19:52 GMT  
		Size: 443.4 KB (443405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0517bc00bb190b33d145488299238da1a6c4b3a3d6819bb8e145141d9f299cfb`  
		Last Modified: Thu, 03 Mar 2022 21:19:51 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
