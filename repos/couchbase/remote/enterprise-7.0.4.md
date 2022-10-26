## `couchbase:enterprise-7.0.4`

```console
$ docker pull couchbase@sha256:d6cf4a2b0242bf007044bd37f234ffbe9ca942a6c54362d2fe4ed12e20cd415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.4` - linux; amd64

```console
$ docker pull couchbase@sha256:71fb111195b63c10706916be1ad7b3698feab754f8d825bd53465ba61b066865
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 MB (641144713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4057935ef652cb455afdbba6979d8c5da333c238be8700dbf66bcbc0f5308306`
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
# Tue, 25 Oct 2022 16:00:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4
# Tue, 25 Oct 2022 16:00:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb
# Tue, 25 Oct 2022 16:00:04 GMT
ARG CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2
# Tue, 25 Oct 2022 16:00:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 25 Oct 2022 16:00:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4 CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 25 Oct 2022 16:01:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4 CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 16:01:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4 CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 25 Oct 2022 16:01:10 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 25 Oct 2022 16:01:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4 CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 25 Oct 2022 16:01:11 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 25 Oct 2022 16:01:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4 CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 25 Oct 2022 16:01:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.4 CB_SHA256=dfa3c2eec3cbf31ee200eb1423f4b19719edd0b73fdf1132956302462b74a9b2 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 25 Oct 2022 16:01:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 25 Oct 2022 16:01:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 16:01:20 GMT
CMD ["couchbase-server"]
# Tue, 25 Oct 2022 16:01:20 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 25 Oct 2022 16:01:20 GMT
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
	-	`sha256:b721765bd8b217c7e6cba34e67870c5ec9bf70c98fefe329ccb9cb83d2601882`  
		Last Modified: Wed, 26 Oct 2022 16:51:03 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b41437b4d2ff3aebf3bd7a962b92277c45591a336cc9593668ff98223374ce`  
		Last Modified: Wed, 26 Oct 2022 16:52:13 GMT  
		Size: 605.9 MB (605886279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714586bd2b50af99294746d64b267176beba2a9cf0003d693057a0444675f07b`  
		Last Modified: Wed, 26 Oct 2022 16:51:03 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c38ade4c9b7c5146cbabbddae4872f9522cced7d85822dbca4cd19e803cd173`  
		Last Modified: Wed, 26 Oct 2022 16:51:03 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ca43614252475fcf58c1bb0282ae4ba3671fde7a821e885ffbd2f844182760`  
		Last Modified: Wed, 26 Oct 2022 16:51:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f286529e7e94c2e506cbea84305b9d557e2a706096adaaa800aed7b2a2e122`  
		Last Modified: Wed, 26 Oct 2022 16:51:01 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a7b8b97d075ff4360d87fc77fe822f4c468d17fd861bdfccaa5d5c60961a1b`  
		Last Modified: Wed, 26 Oct 2022 16:51:01 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e09ed2dc9f67d55bbdf5be3e0f608b555026cc136334568a1e9fdc297228861`  
		Last Modified: Wed, 26 Oct 2022 16:51:01 GMT  
		Size: 444.0 KB (444007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f1a51f1251359f974bc9ed7d5529490e5cb50cce656313b0005693299ef49a`  
		Last Modified: Wed, 26 Oct 2022 16:51:00 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
