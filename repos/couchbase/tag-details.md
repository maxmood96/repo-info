<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.6.5`](#couchbase665)
-	[`couchbase:7.0.3`](#couchbase703)
-	[`couchbase:7.1.1`](#couchbase711)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:community-7.1.1`](#couchbasecommunity-711)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.6.5`](#couchbaseenterprise-665)
-	[`couchbase:enterprise-7.0.3`](#couchbaseenterprise-703)
-	[`couchbase:enterprise-7.1.1`](#couchbaseenterprise-711)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.6.5`

```console
$ docker pull couchbase@sha256:48f013fef13eafd97d891143879f4f8d7457b61b88eb86156d68862aa81242bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:65bd76310fb88858c1072e77f8d226538097e2e9e7de34f9ebdb476687372e4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.9 MB (540920522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4621d41ad0b0f972fced764f0391b68ded53b6678a6a5cc9806d06448b6c1e7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_PACKAGE_NAME=couchbase-server
# Thu, 16 Jun 2022 19:19:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jun 2022 19:19:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jun 2022 19:21:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && dpkg --unpack ./$CB_PACKAGE     && sed -i -e '/Best heuristic/ a \ \ \ \ [ -d /run/systemd/system ] && return 1; return 0' /opt/couchbase/bin/install/systemd-ctl     && dpkg --configure couchbase-server     && apt-get install -yf     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 16 Jun 2022 19:21:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 16 Jun 2022 19:21:57 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 16 Jun 2022 19:21:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 16 Jun 2022 19:21:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jun 2022 19:21:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jun 2022 19:22:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 16 Jun 2022 19:22:06 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 16 Jun 2022 19:22:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jun 2022 19:22:07 GMT
CMD ["couchbase-server"]
# Thu, 16 Jun 2022 19:22:07 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jun 2022 19:22:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04900e67c7722e1bdebeb75923831ffb09cd4144e658f936655fe88b65fe53`  
		Last Modified: Thu, 16 Jun 2022 19:24:12 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d29b463b97a6c658efa4f88867fa5e6da24a67eaec9a73d4c65e8e8eb0d7f`  
		Last Modified: Thu, 16 Jun 2022 19:25:04 GMT  
		Size: 505.7 MB (505652209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6012d2c044c2dcbc4579fc135c4b8d699d148071cd2126bcc0bab0e462811bc`  
		Last Modified: Thu, 16 Jun 2022 19:24:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42558ebd0d9a537833639c2f5b2be7ab4ae9fe59e262a870ad8dacbd8c53a4f3`  
		Last Modified: Thu, 16 Jun 2022 19:24:12 GMT  
		Size: 746.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709bc4f4ad3136f3dbf02318edc8cebb92e4884a4fe3e8344484e8828f2544e2`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acd617ad886616df9dec77c1b67a0d80dcee8802b357f85acdf590ab4d790bd`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619130a9cfaf9c767122575fe77ffb309a4b6e7515020ed2f2d5980f692cef55`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b1383317400dc28be2794b328f0298dff3a0151356053d3f22798f90a494b4`  
		Last Modified: Thu, 16 Jun 2022 19:24:10 GMT  
		Size: 439.6 KB (439563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9184f1c4ccb52dd02b56e7b489c9b650019e039b60b11e7429a9b0c5783e65c`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.3`

```console
$ docker pull couchbase@sha256:4467820a8135bfcb72bc800be57fb55fca97c6e541f27f5922d5ae20f373009f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:4d4a5db4a5e707335ac1b336a35b4c7add23d098d0da058be9570bc16bdd0ef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653570446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99931c68e2f8b48bb6cc411bcd68d32ac72d88b7f6c573d7e4180a4ebe8636f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:59:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1
# Mon, 06 Jun 2022 23:59:36 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:59:36 GMT
ARG CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f
# Mon, 06 Jun 2022 23:59:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:59:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jun 2022 00:00:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 07 Jun 2022 00:00:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 07 Jun 2022 00:00:44 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 07 Jun 2022 00:00:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 07 Jun 2022 00:00:44 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jun 2022 00:00:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jun 2022 00:00:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 07 Jun 2022 00:00:52 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 07 Jun 2022 00:00:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jun 2022 00:00:52 GMT
CMD ["couchbase-server"]
# Tue, 07 Jun 2022 00:00:52 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jun 2022 00:00:52 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2232bc68c4ccdb716a897e650718d528a7e85be0f84c1a555a2b854ff447d555`  
		Last Modified: Tue, 07 Jun 2022 00:09:56 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dcadddc5f7ab4cfec6978fd82c04ef39e0e60d25fd91c86c014f92e59f1cfc`  
		Last Modified: Tue, 07 Jun 2022 00:11:01 GMT  
		Size: 618.3 MB (618297854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058963b53d7b0b16a3f601ac11d8ad2f56fc0235146543b73e72700c8ecbafa6`  
		Last Modified: Tue, 07 Jun 2022 00:09:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e117c91ec6105a20256ecc31a80dd343b9696b5ab868d18dd7418d71bb15873c`  
		Last Modified: Tue, 07 Jun 2022 00:09:56 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eb38cc3021ef93bda00c2b49c4e299f0041cf40176a4a9d6c13f6905219d2`  
		Last Modified: Tue, 07 Jun 2022 00:09:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4c56424e3b39076559b294b3945cb04646b5542ed45a97dbaf2fc3ed479ad4`  
		Last Modified: Tue, 07 Jun 2022 00:09:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1478946131cdf6d66b8b1ac3d21a21bcb8433de52c1bf3c713ba90ee8b55000`  
		Last Modified: Tue, 07 Jun 2022 00:09:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e1af61fc7e550529762d2b7f0c4d7f6f416494e0fba8b77b8e1a4459579d80`  
		Last Modified: Tue, 07 Jun 2022 00:09:54 GMT  
		Size: 443.9 KB (443867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368869fbe8323188369ff3fe5a55ee60b53bb8af603d16322ad03f05d01d8fb7`  
		Last Modified: Tue, 07 Jun 2022 00:09:54 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.1.1`

**does not exist** (yet?)

## `couchbase:community`

```console
$ docker pull couchbase@sha256:c5a18e2523c0df3f33cf628951ca40eeeb770d18c1b6bd5c40cc306f756b2136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:ecdf66c68f0ed58f9c8ee7d9f99d4ffbd3cef85eccea1d691fc4fc946f6558fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349044603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42453a1704198596fd5f4de8d57c88ac7f7a8d60a2460314d463e4b49de84380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0
# Mon, 06 Jun 2022 23:58:52 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:58:52 GMT
ARG CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539
# Mon, 06 Jun 2022 23:58:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:58:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 06 Jun 2022 23:59:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:59:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 06 Jun 2022 23:59:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 06 Jun 2022 23:59:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Mon, 06 Jun 2022 23:59:32 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 06 Jun 2022 23:59:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 06 Jun 2022 23:59:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=23c24973c9a9c57341bd78549dc8b07b149b3c3798bfa0968b77678c47b7f539 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 06 Jun 2022 23:59:33 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Mon, 06 Jun 2022 23:59:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jun 2022 23:59:33 GMT
CMD ["couchbase-server"]
# Mon, 06 Jun 2022 23:59:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Mon, 06 Jun 2022 23:59:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f066d477269a208fd593affb5665c2128daf8dee05f6312fb50971cff31fb434`  
		Last Modified: Tue, 07 Jun 2022 00:09:03 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6edf1cedda40fa9e51d92d21c021bc9a2bee9070c3c8c4205cfa04c1d5012`  
		Last Modified: Tue, 07 Jun 2022 00:09:44 GMT  
		Size: 314.2 MB (314215876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d26a3f9a09c47cb4eda07e4502823fb8bb0d880cc51f23e64e71f8bdb15b58`  
		Last Modified: Tue, 07 Jun 2022 00:09:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f464fe501c0d90ae2ab29f501a811632e9423afe0d23b1c45c78a4bc4d380d`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2c00d03227fa4feb5e8d36d73f2797f4d75c420c798dbafbfa22105e5dc61c`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dcd7e1d853f91ebad23cc758a89935314030c7f598fc15f1fa307287688f51`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef3d656bc7708dc688b5ce04f1ebf0571df2fee448fa0cb7ba3de8c1c8d11ae`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800d564395e484973e7b383c43913b150ef28bfb4e969c341a7cf822445c236d`  
		Last Modified: Tue, 07 Jun 2022 00:09:01 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:152872615c166abe1670a9bba9e06e33203a93c03b0d4318a0a2437420264af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:af6e724bdc0e372140c00a8792b249e4a2646a50b1b8b4b827fd4a519edb2766
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352545387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ec99728f639027de93b9332313b8915a5f7e2449a57a474f1ee5abdb912780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Thu, 16 Jun 2022 19:22:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 16 Jun 2022 19:22:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 16 Jun 2022 19:22:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jun 2022 19:22:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 16 Jun 2022 19:22:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 16 Jun 2022 19:22:32 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Thu, 16 Jun 2022 19:22:32 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Thu, 16 Jun 2022 19:22:32 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 16 Jun 2022 19:22:32 GMT
ARG CB_PACKAGE_NAME=couchbase-server-community
# Thu, 16 Jun 2022 19:22:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jun 2022 19:22:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jun 2022 19:23:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && dpkg --unpack ./$CB_PACKAGE     && sed -i -e '/Best heuristic/ a \ \ \ \ [ -d /run/systemd/system ] && return 1; return 0' /opt/couchbase/bin/install/systemd-ctl     && dpkg --configure couchbase-server-community     && apt-get install -yf     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 16 Jun 2022 19:23:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 16 Jun 2022 19:23:33 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 16 Jun 2022 19:23:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 16 Jun 2022 19:23:34 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jun 2022 19:23:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jun 2022 19:23:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 16 Jun 2022 19:23:43 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 16 Jun 2022 19:23:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jun 2022 19:23:43 GMT
CMD ["couchbase-server"]
# Thu, 16 Jun 2022 19:23:43 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jun 2022 19:23:43 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55862d623ee91aabe20b5cc2a4e5acf880a3a7505463ffa3f6988d708c4ecf61`  
		Last Modified: Thu, 16 Jun 2022 19:25:18 GMT  
		Size: 5.6 MB (5632708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75091c0a976aa6e1402f435bf54265652e1a3abbd42c8b0717d4032912761523`  
		Last Modified: Thu, 16 Jun 2022 19:25:16 GMT  
		Size: 2.0 KB (1973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3cf07404138e64cc40902da3b1615bc544f4657344eb849af69cb670feb95b`  
		Last Modified: Thu, 16 Jun 2022 19:25:52 GMT  
		Size: 319.8 MB (319763088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafafe63e471e7422eba58370186d199497a388ff491d7953c716718ba7d44fb`  
		Last Modified: Thu, 16 Jun 2022 19:25:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d456f82844ce25cb517366caeb2a207b6377243e5700529d45cbaf6f70800707`  
		Last Modified: Thu, 16 Jun 2022 19:25:16 GMT  
		Size: 742.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5593bd64a7e67abcffe384f1193bdecaec4b83aa0dff9773997a4f85213372fc`  
		Last Modified: Thu, 16 Jun 2022 19:25:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6581fa390cb7679a577b100d61c97240b876cc6942cd4352665a27f3544461`  
		Last Modified: Thu, 16 Jun 2022 19:25:14 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3a91c654c961e30d0647aee83a96d55006714bd70bf3dba0f6933368f87aa`  
		Last Modified: Thu, 16 Jun 2022 19:25:14 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87832a5a92571c91731bf84fea6de7925c336356fdfe05bd690d8b44d3a72ec3`  
		Last Modified: Thu, 16 Jun 2022 19:25:15 GMT  
		Size: 433.5 KB (433461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb7d993ed2b033ec320fd2fa50a10fe112cc3026684eea26b57c58458ec0319`  
		Last Modified: Thu, 16 Jun 2022 19:25:14 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:e751f95d4943de0a5f98b3161a869781482e88b08dee7c5d8cdf56f052ec5d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:060e0fe50aa66b4fae7d97cac3c72b9cf2755ac7bae081115f2515bb270e5838
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429030057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b2be9a022e359c1363e303bf422ae8d528d5b193781ee0c4c0c2437ae794ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Jun 2022 00:01:09 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jun 2022 00:01:10 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Tue, 07 Jun 2022 00:01:10 GMT
ARG CB_VERSION=7.0.2
# Tue, 07 Jun 2022 00:01:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Tue, 07 Jun 2022 00:01:10 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Tue, 07 Jun 2022 00:01:10 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Tue, 07 Jun 2022 00:01:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jun 2022 00:01:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jun 2022 00:01:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jun 2022 00:01:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 07 Jun 2022 00:01:58 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Tue, 07 Jun 2022 00:01:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 07 Jun 2022 00:01:59 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jun 2022 00:01:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jun 2022 00:02:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jun 2022 00:02:00 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jun 2022 00:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jun 2022 00:02:00 GMT
CMD ["couchbase-server"]
# Tue, 07 Jun 2022 00:02:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jun 2022 00:02:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9b08b71f1099781ce3d94fddfa48700f5064d618edbfb40a3bb4af11cc6d10`  
		Last Modified: Tue, 07 Jun 2022 00:11:19 GMT  
		Size: 6.3 MB (6261600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526c7b0820871ac396d389bedfc7a04a2898d8c59c70e6a6bacadea2aa1624db`  
		Last Modified: Tue, 07 Jun 2022 00:11:16 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e62ea5aed98302048aa5091b329b0f91fec1333647e04d2ca1fd85624ef76af`  
		Last Modified: Tue, 07 Jun 2022 00:11:16 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022e41e29de061937434e5e06a9f147817c83ba2c6bbb794dbf64b05de47b6d8`  
		Last Modified: Tue, 07 Jun 2022 00:12:03 GMT  
		Size: 394.1 MB (394061837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f38ea995720876e556a202fac82a8f837bf4c2b47f0bfa9adffd40e0d74e31`  
		Last Modified: Tue, 07 Jun 2022 00:11:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ec3c7130fb78fd124164a97e0516c9b956cd5cf2b6cf6040df61114f7ad5c2`  
		Last Modified: Tue, 07 Jun 2022 00:11:15 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc019282e22e3fd66e1154918bc1507a25058983cb204523c00bf4483d27891`  
		Last Modified: Tue, 07 Jun 2022 00:11:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0faaa8b368d5d2077d7ffb840f0adeade1ff7ac0da6ddb58e8614940d655b09`  
		Last Modified: Tue, 07 Jun 2022 00:11:13 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e9490b59283c7f7b0611784d5cab8759ef60142e2a4ae400aa04eb859376c6`  
		Last Modified: Tue, 07 Jun 2022 00:11:13 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db64d692de218c7cc6d34021b913c2b6044318b2d2733e54fac7df22d5772be6`  
		Last Modified: Tue, 07 Jun 2022 00:11:13 GMT  
		Size: 129.5 KB (129506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f1f9c59ce0d0595f7dc1bd7fa6556c31bdb5a6eed8075cd9a08c88c8735a3f`  
		Last Modified: Tue, 07 Jun 2022 00:11:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.1.1`

**does not exist** (yet?)

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:6ea8fc49bde775bb4999f59add71dc7e016c7ec6c00a286729c395a1948c0356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:7d39eec7f4b690434d612729e20696704b35af5c65a7452384f7f2ccb4e2e3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597284519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d89249226d96836b0a13f648400b9189386bc13965b7d75467689b363de3bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987
# Mon, 06 Jun 2022 23:57:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:57:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 06 Jun 2022 23:58:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 06 Jun 2022 23:58:43 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 06 Jun 2022 23:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Mon, 06 Jun 2022 23:58:44 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 06 Jun 2022 23:58:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 06 Jun 2022 23:58:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 06 Jun 2022 23:58:45 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Mon, 06 Jun 2022 23:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jun 2022 23:58:45 GMT
CMD ["couchbase-server"]
# Mon, 06 Jun 2022 23:58:45 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Mon, 06 Jun 2022 23:58:45 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382f188a254365de856786d2674ede0de9879c8ccbb6afd090f339672983369`  
		Last Modified: Tue, 07 Jun 2022 00:07:46 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70907b514b578a504619d3d14792edbf0202a0f1f7758baffd0e5660ebad329`  
		Last Modified: Tue, 07 Jun 2022 00:08:45 GMT  
		Size: 562.5 MB (562455802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef166d73a55b945bf9c1d80fad208364b8090aaad90081f952a5c865258e94`  
		Last Modified: Tue, 07 Jun 2022 00:07:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437177da346d5fa18219c10d2749a25ef125f4de4b702b4fff7a14a5a31bccc`  
		Last Modified: Tue, 07 Jun 2022 00:07:43 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de991ce42e47127d35719b69d6eb8e7930f66ddc424d1fe6eefbf4f0712beed7`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b527c1f51ff4a3db59ecb458830ad9722d0604474ac83ed472d002c4a37570`  
		Last Modified: Tue, 07 Jun 2022 00:07:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebba9d2f225c927231971398e9dde38cb5280e95f5cd018b0db26c1dac7aa98`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d9f0e42e30d39153e6c61c707e551e1f90909cfc66bfa8ae986c3ac5ccb42`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.6.5`

```console
$ docker pull couchbase@sha256:48f013fef13eafd97d891143879f4f8d7457b61b88eb86156d68862aa81242bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:65bd76310fb88858c1072e77f8d226538097e2e9e7de34f9ebdb476687372e4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.9 MB (540920522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4621d41ad0b0f972fced764f0391b68ded53b6678a6a5cc9806d06448b6c1e7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 16 Jun 2022 19:19:34 GMT
ARG CB_PACKAGE_NAME=couchbase-server
# Thu, 16 Jun 2022 19:19:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jun 2022 19:19:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jun 2022 19:21:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && dpkg --unpack ./$CB_PACKAGE     && sed -i -e '/Best heuristic/ a \ \ \ \ [ -d /run/systemd/system ] && return 1; return 0' /opt/couchbase/bin/install/systemd-ctl     && dpkg --configure couchbase-server     && apt-get install -yf     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 16 Jun 2022 19:21:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 16 Jun 2022 19:21:57 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 16 Jun 2022 19:21:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 16 Jun 2022 19:21:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jun 2022 19:21:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jun 2022 19:22:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_PACKAGE_NAME=couchbase-server CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 16 Jun 2022 19:22:06 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 16 Jun 2022 19:22:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jun 2022 19:22:07 GMT
CMD ["couchbase-server"]
# Thu, 16 Jun 2022 19:22:07 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jun 2022 19:22:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c04900e67c7722e1bdebeb75923831ffb09cd4144e658f936655fe88b65fe53`  
		Last Modified: Thu, 16 Jun 2022 19:24:12 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d29b463b97a6c658efa4f88867fa5e6da24a67eaec9a73d4c65e8e8eb0d7f`  
		Last Modified: Thu, 16 Jun 2022 19:25:04 GMT  
		Size: 505.7 MB (505652209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6012d2c044c2dcbc4579fc135c4b8d699d148071cd2126bcc0bab0e462811bc`  
		Last Modified: Thu, 16 Jun 2022 19:24:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42558ebd0d9a537833639c2f5b2be7ab4ae9fe59e262a870ad8dacbd8c53a4f3`  
		Last Modified: Thu, 16 Jun 2022 19:24:12 GMT  
		Size: 746.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709bc4f4ad3136f3dbf02318edc8cebb92e4884a4fe3e8344484e8828f2544e2`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acd617ad886616df9dec77c1b67a0d80dcee8802b357f85acdf590ab4d790bd`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619130a9cfaf9c767122575fe77ffb309a4b6e7515020ed2f2d5980f692cef55`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b1383317400dc28be2794b328f0298dff3a0151356053d3f22798f90a494b4`  
		Last Modified: Thu, 16 Jun 2022 19:24:10 GMT  
		Size: 439.6 KB (439563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9184f1c4ccb52dd02b56e7b489c9b650019e039b60b11e7429a9b0c5783e65c`  
		Last Modified: Thu, 16 Jun 2022 19:24:09 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.3`

```console
$ docker pull couchbase@sha256:4467820a8135bfcb72bc800be57fb55fca97c6e541f27f5922d5ae20f373009f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:4d4a5db4a5e707335ac1b336a35b4c7add23d098d0da058be9570bc16bdd0ef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653570446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99931c68e2f8b48bb6cc411bcd68d32ac72d88b7f6c573d7e4180a4ebe8636f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:59:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1
# Mon, 06 Jun 2022 23:59:36 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:59:36 GMT
ARG CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f
# Mon, 06 Jun 2022 23:59:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:59:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jun 2022 00:00:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 07 Jun 2022 00:00:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 07 Jun 2022 00:00:44 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 07 Jun 2022 00:00:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 07 Jun 2022 00:00:44 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jun 2022 00:00:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jun 2022 00:00:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-MP1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3-MP1 CB_SHA256=a1bfcc476e01c71a212c2ed5026f24f3df01b3591c24dcf45678fdb2625cfc0f CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 07 Jun 2022 00:00:52 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 07 Jun 2022 00:00:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jun 2022 00:00:52 GMT
CMD ["couchbase-server"]
# Tue, 07 Jun 2022 00:00:52 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jun 2022 00:00:52 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2232bc68c4ccdb716a897e650718d528a7e85be0f84c1a555a2b854ff447d555`  
		Last Modified: Tue, 07 Jun 2022 00:09:56 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dcadddc5f7ab4cfec6978fd82c04ef39e0e60d25fd91c86c014f92e59f1cfc`  
		Last Modified: Tue, 07 Jun 2022 00:11:01 GMT  
		Size: 618.3 MB (618297854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058963b53d7b0b16a3f601ac11d8ad2f56fc0235146543b73e72700c8ecbafa6`  
		Last Modified: Tue, 07 Jun 2022 00:09:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e117c91ec6105a20256ecc31a80dd343b9696b5ab868d18dd7418d71bb15873c`  
		Last Modified: Tue, 07 Jun 2022 00:09:56 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eb38cc3021ef93bda00c2b49c4e299f0041cf40176a4a9d6c13f6905219d2`  
		Last Modified: Tue, 07 Jun 2022 00:09:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4c56424e3b39076559b294b3945cb04646b5542ed45a97dbaf2fc3ed479ad4`  
		Last Modified: Tue, 07 Jun 2022 00:09:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1478946131cdf6d66b8b1ac3d21a21bcb8433de52c1bf3c713ba90ee8b55000`  
		Last Modified: Tue, 07 Jun 2022 00:09:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e1af61fc7e550529762d2b7f0c4d7f6f416494e0fba8b77b8e1a4459579d80`  
		Last Modified: Tue, 07 Jun 2022 00:09:54 GMT  
		Size: 443.9 KB (443867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368869fbe8323188369ff3fe5a55ee60b53bb8af603d16322ad03f05d01d8fb7`  
		Last Modified: Tue, 07 Jun 2022 00:09:54 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.1.1`

**does not exist** (yet?)

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:6ea8fc49bde775bb4999f59add71dc7e016c7ec6c00a286729c395a1948c0356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:7d39eec7f4b690434d612729e20696704b35af5c65a7452384f7f2ccb4e2e3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597284519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d89249226d96836b0a13f648400b9189386bc13965b7d75467689b363de3bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987
# Mon, 06 Jun 2022 23:57:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:57:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 06 Jun 2022 23:58:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 06 Jun 2022 23:58:43 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 06 Jun 2022 23:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Mon, 06 Jun 2022 23:58:44 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 06 Jun 2022 23:58:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 06 Jun 2022 23:58:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 06 Jun 2022 23:58:45 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Mon, 06 Jun 2022 23:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jun 2022 23:58:45 GMT
CMD ["couchbase-server"]
# Mon, 06 Jun 2022 23:58:45 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Mon, 06 Jun 2022 23:58:45 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382f188a254365de856786d2674ede0de9879c8ccbb6afd090f339672983369`  
		Last Modified: Tue, 07 Jun 2022 00:07:46 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70907b514b578a504619d3d14792edbf0202a0f1f7758baffd0e5660ebad329`  
		Last Modified: Tue, 07 Jun 2022 00:08:45 GMT  
		Size: 562.5 MB (562455802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef166d73a55b945bf9c1d80fad208364b8090aaad90081f952a5c865258e94`  
		Last Modified: Tue, 07 Jun 2022 00:07:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437177da346d5fa18219c10d2749a25ef125f4de4b702b4fff7a14a5a31bccc`  
		Last Modified: Tue, 07 Jun 2022 00:07:43 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de991ce42e47127d35719b69d6eb8e7930f66ddc424d1fe6eefbf4f0712beed7`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b527c1f51ff4a3db59ecb458830ad9722d0604474ac83ed472d002c4a37570`  
		Last Modified: Tue, 07 Jun 2022 00:07:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebba9d2f225c927231971398e9dde38cb5280e95f5cd018b0db26c1dac7aa98`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d9f0e42e30d39153e6c61c707e551e1f90909cfc66bfa8ae986c3ac5ccb42`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
