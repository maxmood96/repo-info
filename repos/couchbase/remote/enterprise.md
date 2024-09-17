## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:78446fa1cf1c9cea6c563114b7882b5c3f84d1663207b15dd966bf8f10b427c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:4342083b374e46237b9ba1ae162a2993d8e233c8b7747bd0695c5b0fb7b59325
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.3 MB (770296192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c4ee2319bce3fe1edaf6a320aec0facb31c39163e57f2a01efef7bf6ba46b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:54:12 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 00:54:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 00:54:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 00:54:44 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 17 Sep 2024 00:55:11 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 17 Sep 2024 00:55:12 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Tue, 17 Sep 2024 00:55:12 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 00:55:12 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 00:55:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 00:55:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 17 Sep 2024 00:56:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 00:56:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 17 Sep 2024 00:56:50 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Tue, 17 Sep 2024 00:56:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 17 Sep 2024 00:56:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 17 Sep 2024 00:56:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 17 Sep 2024 00:56:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 17 Sep 2024 00:56:52 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 17 Sep 2024 00:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 00:56:53 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 00:56:53 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 17 Sep 2024 00:56:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3160f1a6e4b8ff701d41f4e4c8d9a4b1c1592ef1004cca81307abdf1034fdc0`  
		Last Modified: Tue, 17 Sep 2024 00:57:43 GMT  
		Size: 39.3 MB (39286551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579a2713d98aff2a687085ede37664a92d7956c149839b259df41bad8a2da9de`  
		Last Modified: Tue, 17 Sep 2024 00:57:37 GMT  
		Size: 1.2 MB (1154878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8958e6669379e26ffe3100a0128d832b4013f78dd01e2f9a7b4f91fb9df37d`  
		Last Modified: Tue, 17 Sep 2024 00:57:36 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d0f4b1457a669678691fc3fe031c645be0c8c38853c6dbe60cb134388ea677`  
		Last Modified: Tue, 17 Sep 2024 00:58:42 GMT  
		Size: 699.4 MB (699409614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8b61e5c967803a72742c08412534024c5a735dbde5d5fbd614e656ba7f1417`  
		Last Modified: Tue, 17 Sep 2024 00:57:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4574f9452590a49174efbb7735bc50e147528cd3cac84ec77581daf42278c8`  
		Last Modified: Tue, 17 Sep 2024 00:57:34 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd58538892224f828d27b8601c5bc226a3598c7893448fec98a4b31b6da8f8b`  
		Last Modified: Tue, 17 Sep 2024 00:57:34 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c4435ce786b92fb5b6452cc3a854ca68cd872803ad913fcf7bc24b2fa57056`  
		Last Modified: Tue, 17 Sep 2024 00:57:34 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feffaa967046172cff36a80c4265651ab77872b9cbdb0a80af25e7c399d324e6`  
		Last Modified: Tue, 17 Sep 2024 00:57:34 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a8bf1726d011db16fa8e17d075f018755b4fda80e7da65d48ad9efbc454fa9`  
		Last Modified: Tue, 17 Sep 2024 00:57:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:b64af89661d06c931a7203df757c5e1cc6e98282aa285ec56634721b2bc19b92
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.8 MB (741773866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076226edc7e18667173ee2cdd08aab4d9f1393b7c008d021a98b699403cf48f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:11:12 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 01:11:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 01:11:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 01:11:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 17 Sep 2024 01:12:49 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 17 Sep 2024 01:12:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Tue, 17 Sep 2024 01:12:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 01:12:49 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 01:12:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 01:12:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 17 Sep 2024 01:14:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 01:14:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 17 Sep 2024 01:14:15 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Tue, 17 Sep 2024 01:14:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 17 Sep 2024 01:14:16 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 17 Sep 2024 01:14:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 17 Sep 2024 01:14:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 17 Sep 2024 01:14:17 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 17 Sep 2024 01:14:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 01:14:17 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 01:14:17 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 17 Sep 2024 01:14:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f47af7f54d2f0b0b91182f0e57e09d631f33b353936c38969c8fb8a1d3cd`  
		Last Modified: Tue, 17 Sep 2024 01:14:47 GMT  
		Size: 38.8 MB (38829529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b0c58c39b9f6e5107c6a335dd39461a876d38b3d4ec297b969abe154602fc9`  
		Last Modified: Tue, 17 Sep 2024 01:14:42 GMT  
		Size: 999.8 KB (999815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e9b370f594259ebb1d000e9268d0e7bdb87b744265eff4f628b9d793e65431`  
		Last Modified: Tue, 17 Sep 2024 01:14:41 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed78ca14ad1d692e77487301d37699dfbd47c0b8640fdc4d01d61f9fe18b9aa9`  
		Last Modified: Tue, 17 Sep 2024 01:15:28 GMT  
		Size: 673.5 MB (673542191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5671e02dad6c60340203e9f3a734c669b05b198db468ffeb752bf54c648a50d3`  
		Last Modified: Tue, 17 Sep 2024 01:14:41 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3873c10fbd13663d2c3f13df48aa4f608a9974853f19fcfd7fb4882f5a36cfb0`  
		Last Modified: Tue, 17 Sep 2024 01:14:40 GMT  
		Size: 821.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cf2d31d997678559549dc1dc284386ab215a84cf959989e3e548032720dee0`  
		Last Modified: Tue, 17 Sep 2024 01:14:39 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ed722984a97439788241352cca972ec3c406be4933ad7c8520329870539a2`  
		Last Modified: Tue, 17 Sep 2024 01:14:39 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dfc3f907d0e40690ab0aaa3d98220d8da185bad1b71e370034ee282a28b535`  
		Last Modified: Tue, 17 Sep 2024 01:14:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5189f0e22304813a0c7f2a242435e3565aba8055716b800f6a8de871c88d34`  
		Last Modified: Tue, 17 Sep 2024 01:14:40 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
