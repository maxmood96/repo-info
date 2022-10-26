## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:c0412a6132ae1935936a319c69d114b2bd9fd38bd883bef432d2755a5bac7723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:9a17dfed86c1b96b2431e3bbf5705a38938826afd26884850a996c156cf22b3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352539595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f2ecc7c1d1a8125c5eee0ac919ccafcf279b235374a70bedb052ac4ede914`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:04:13 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 25 Oct 2022 16:04:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 25 Oct 2022 16:04:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 16:04:33 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 25 Oct 2022 16:04:33 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Tue, 25 Oct 2022 16:04:33 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Tue, 25 Oct 2022 16:04:33 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Tue, 25 Oct 2022 16:04:33 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 25 Oct 2022 16:04:33 GMT
ARG CB_PACKAGE_NAME=couchbase-server-community
# Tue, 25 Oct 2022 16:04:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 25 Oct 2022 16:04:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 25 Oct 2022 16:05:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && dpkg --unpack ./$CB_PACKAGE     && sed -i -e '/Best heuristic/ a \ \ \ \ [ -d /run/systemd/system ] && return 1; return 0' /opt/couchbase/bin/install/systemd-ctl     && dpkg --configure couchbase-server-community     && apt-get install -yf     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 16:05:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 25 Oct 2022 16:05:22 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 25 Oct 2022 16:05:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 25 Oct 2022 16:05:23 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 25 Oct 2022 16:05:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 25 Oct 2022 16:05:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_PACKAGE_NAME=couchbase-server-community CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 25 Oct 2022 16:05:32 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 25 Oct 2022 16:05:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 16:05:32 GMT
CMD ["couchbase-server"]
# Tue, 25 Oct 2022 16:05:32 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 25 Oct 2022 16:05:32 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208cfd618a6f00b928bd89942d5bbae43376ec07407d87a04638170ec63ce345`  
		Last Modified: Wed, 26 Oct 2022 16:54:40 GMT  
		Size: 5.6 MB (5626020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f07539bbbff2f694a6707bbe685dbd2267d2062e79dcf28b25dc80df221236`  
		Last Modified: Wed, 26 Oct 2022 16:54:38 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4df477c9e2baa454a6222d1bcc442413ec364ebe55aafe7c665248aacae2a3`  
		Last Modified: Wed, 26 Oct 2022 16:55:17 GMT  
		Size: 319.8 MB (319763159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01ea00f48ef935d97f1d78050237fcc0da4007dbb0f0392424b2c0ca3a31eb`  
		Last Modified: Wed, 26 Oct 2022 16:54:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d474b7caf1f9363f7360f46da7d413785402649c875a0f916a309d2e8b87649e`  
		Last Modified: Wed, 26 Oct 2022 16:54:38 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a1a499f9dc7401ea1d6f5dbd6f69447c4a328a523d65fc88dffecf2a52ee21`  
		Last Modified: Wed, 26 Oct 2022 16:54:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd8ac63b78a0cfbca47e079e59436adac2eb8fbf265e12c03dc073021d5fa38`  
		Last Modified: Wed, 26 Oct 2022 16:54:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f5aeecbf6c17535c3dfb29b779f81823acc9c522f7fbcb255cf5e9e0084c43`  
		Last Modified: Wed, 26 Oct 2022 16:54:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf39ef07fa292f2547f9cd55ffa3cfbf4ee05ddbae57c6192ee81f0566a6409`  
		Last Modified: Wed, 26 Oct 2022 16:54:36 GMT  
		Size: 433.4 KB (433424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3055d2c1dbd8eec5002f7e1cbdd1a1d0af67ca540d33d2d8dcacce840c60c302`  
		Last Modified: Wed, 26 Oct 2022 16:54:36 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
