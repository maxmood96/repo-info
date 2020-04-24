## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:c3d1ae93a0a8768f5c0a4e37a41434f296ad1bacbc80f6d715d8787e67839a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:10b655bf66aa8f74dc12da16316266b743ded6cdb60cc47b7c184ff3fc4fbf1e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.3 MB (522267604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5564ad5e4af2c152ccacf105c5aec625f468ce31dcb8ac0e8a5cd09fda2c353`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 19:38:12 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 19:38:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 24 Apr 2020 19:38:14 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 24 Apr 2020 19:44:32 GMT
RUN apt-get update && apt-get install -q -y     gazebo9=9.13.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 19:44:32 GMT
EXPOSE 11345
# Fri, 24 Apr 2020 19:44:33 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 24 Apr 2020 19:44:33 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 24 Apr 2020 19:44:33 GMT
CMD ["gzserver"]
# Fri, 24 Apr 2020 19:45:55 GMT
RUN apt-get update && apt-get install -q -y     libgazebo9-dev=9.13.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fdea518f641b05b04552c209a92daef48c94c9b1f6857f2476a52e5bd5c67a`  
		Last Modified: Fri, 24 Apr 2020 19:58:15 GMT  
		Size: 16.7 MB (16663975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc6e658a9746cce875a65f439176cd63e4e20154bc73c440f72fecccea9987`  
		Last Modified: Fri, 24 Apr 2020 19:58:12 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c58ff796c9b530927acddfe12f42143186e6130c91be353c95b2d00162895c`  
		Last Modified: Fri, 24 Apr 2020 19:58:11 GMT  
		Size: 5.5 KB (5524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892114c28aee6c67c30d3e6f8c1fa5bafd0f4ac2ca4f6e6b78d18aeb79925678`  
		Last Modified: Fri, 24 Apr 2020 20:00:19 GMT  
		Size: 219.5 MB (219452763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc4dc5b6e09e8c49a6db655a66716798b0848655268bd5380505b30c0f8a40b`  
		Last Modified: Fri, 24 Apr 2020 19:59:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052e51a3b8dac2dcb780d9f46ee562a91fb1812a9776aab2668521348974465f`  
		Last Modified: Fri, 24 Apr 2020 20:01:15 GMT  
		Size: 241.9 MB (241883351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
