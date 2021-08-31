## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:98299b065e5be953e2762a65c4a848f0b153c863b9b4831b5c879bb66ab4d86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:dbe90ce9e946168227833c090d4719986d63aa17e2eb4bb5a73b9c619ed2311f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466125041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1672e6f2e19e654639ea62a998982902461bc803be7694258c54cd3b646c8c22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:21:37 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 31 Aug 2021 03:23:42 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:23:43 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Tue, 31 Aug 2021 03:23:43 GMT
ARG CB_VERSION=6.0.5
# Tue, 31 Aug 2021 03:23:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Tue, 31 Aug 2021 03:23:43 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Tue, 31 Aug 2021 03:23:43 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Tue, 31 Aug 2021 03:23:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 31 Aug 2021 03:23:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 31 Aug 2021 03:24:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:24:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 31 Aug 2021 03:24:36 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 31 Aug 2021 03:24:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 31 Aug 2021 03:24:37 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 31 Aug 2021 03:24:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 31 Aug 2021 03:24:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 31 Aug 2021 03:24:39 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 31 Aug 2021 03:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Aug 2021 03:24:39 GMT
CMD ["couchbase-server"]
# Tue, 31 Aug 2021 03:24:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 31 Aug 2021 03:24:40 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad2462e90bbb875192fc60ad73a37767fd66736c2d77864c1aa1706277e1b8`  
		Last Modified: Tue, 31 Aug 2021 03:29:31 GMT  
		Size: 15.9 MB (15923740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eade3950f0dac395edba948c8a11be6bb13842c0a0bb507d066d3497a8dd7f9`  
		Last Modified: Tue, 31 Aug 2021 03:29:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3385d6562a5a590e21b076d3556b3a9b913f2a4bb301835793cde88d6ad078`  
		Last Modified: Tue, 31 Aug 2021 03:29:27 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6086cfa42a7e9a96aec888e2245d28d715d9c387136833786b46cc336ef96186`  
		Last Modified: Tue, 31 Aug 2021 03:30:04 GMT  
		Size: 423.4 MB (423362749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692cbc042cd7250d3bff14a5c3b85c853b497afefc270b93349dbba7501519da`  
		Last Modified: Tue, 31 Aug 2021 03:29:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685784ad28283d623e9acaf2e643630dd7f65d6e792e9e13b69569c3536b6121`  
		Last Modified: Tue, 31 Aug 2021 03:29:26 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410d54ee1b88dd20786bdb20fb38cd37d8da77195ce4f99e1b6710ee6b529d43`  
		Last Modified: Tue, 31 Aug 2021 03:29:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcf337856e610d54c62aba78828847d0eaa902e745eaaca762084b16972c8b2`  
		Last Modified: Tue, 31 Aug 2021 03:29:24 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af54e22a6200630e014aa7dc566d5d066d981aa931dcde26108c32a0c6ffd1`  
		Last Modified: Tue, 31 Aug 2021 03:29:23 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea158ae8b16554d05ce26da1c58f180666d03d25e865f71dd42973f5d7aa6ef`  
		Last Modified: Tue, 31 Aug 2021 03:29:24 GMT  
		Size: 125.6 KB (125561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a055e1c798f0e0dc2dfd3b663ff5c85ef232c924ace8e715277f44d7b5d8967`  
		Last Modified: Tue, 31 Aug 2021 03:29:24 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
