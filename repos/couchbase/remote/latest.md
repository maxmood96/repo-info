## `couchbase:latest`

```console
$ docker pull couchbase@sha256:1f64978d304983ad56f01633f54b125b578027c78081dba1125ffa3dd4827753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:b098bb247d5997f89b04e59a8d116b7907ceec457214c757f181128028393af2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597276114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a51ddf314676b32da5a99593490dd62973f7288e261d2b965557eaca576932`
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
# Thu, 05 May 2022 01:19:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb
# Thu, 05 May 2022 01:19:28 GMT
ARG CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987
# Thu, 05 May 2022 01:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 05 May 2022 01:19:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 05 May 2022 01:20:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 05 May 2022 01:20:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 05 May 2022 01:20:42 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 05 May 2022 01:20:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 05 May 2022 01:20:43 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 05 May 2022 01:20:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 05 May 2022 01:20:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 05 May 2022 01:20:44 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 05 May 2022 01:20:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 May 2022 01:20:44 GMT
CMD ["couchbase-server"]
# Thu, 05 May 2022 01:20:44 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 05 May 2022 01:20:44 GMT
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
	-	`sha256:586c5f707c3a620fc5549dc5498b2985d1e70323981d03c391bb819f0ddf782e`  
		Last Modified: Thu, 05 May 2022 01:27:25 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a300a82511ded00c89b320bf40d4dc41b6353621bb463722a116292599adac`  
		Last Modified: Thu, 05 May 2022 01:28:24 GMT  
		Size: 562.5 MB (562454898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf9265b3d00dbaec8fafc81388194a128a75b41c267a1b5534c831931868198`  
		Last Modified: Thu, 05 May 2022 01:27:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9647698da407edfb82a1448c3d1950572e880426326d3bd0d0c6394c77530e7`  
		Last Modified: Thu, 05 May 2022 01:27:22 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeef37ef3ecd46ce3b3eb8bd16a567ad459c7a9fbabe36fcfca85e67e020298`  
		Last Modified: Thu, 05 May 2022 01:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b940aaedabcd56250e0995fdc71e784a6a8a785909821e56ffae8a081add72ca`  
		Last Modified: Thu, 05 May 2022 01:27:22 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f857e3b76d6462751f040e06b53d2f66ec24c31c0175106f765e1e42ba7ea`  
		Last Modified: Thu, 05 May 2022 01:27:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a692084456ff1c924d6eb5576f1efcde656c36bdedc20e6a34f13cf6a12f701`  
		Last Modified: Thu, 05 May 2022 01:27:22 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
