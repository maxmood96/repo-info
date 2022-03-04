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
