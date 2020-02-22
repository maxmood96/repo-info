## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:138407f75bcaea20255a53187f0bfec252cf3f6d7379e9208fdb64f75940982d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:c5e345c8912dca69c86487f6d1bdbade7e6290739f12725669c368bdf02ad9bd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.2 MB (595225137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a02a3591771abf570b736ed6a70623d6eef410c14e4ff943aadb870750fd72`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:33:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:33:46 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:33:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 21 Feb 2020 23:33:48 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 21 Feb 2020 23:42:49 GMT
RUN apt-get update && apt-get install -q -y     gazebo11=11.0.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:42:49 GMT
EXPOSE 11345
# Fri, 21 Feb 2020 23:42:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 21 Feb 2020 23:42:50 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 21 Feb 2020 23:42:50 GMT
CMD ["gzserver"]
# Fri, 21 Feb 2020 23:44:18 GMT
RUN apt-get update && apt-get install -q -y     libgazebo11-dev=11.0.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fe4c16cf9b0d96d5ca63260c28e39ec2082af1f69bdc406d460e68fd3378f0`  
		Last Modified: Fri, 21 Feb 2020 23:47:45 GMT  
		Size: 838.2 KB (838151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa76db183f32be6e5115a1253a816718c7a256d7d6f89282fa48481a4060cbf3`  
		Last Modified: Fri, 21 Feb 2020 23:47:46 GMT  
		Size: 15.1 MB (15149033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e22bb42bd40ce82378ec7a08b6c473e6b6d13236092d24cbcc5719382f150`  
		Last Modified: Fri, 21 Feb 2020 23:47:43 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e545463140ada03ab9e139183557e0d40fddf05d8e9197b3e8970173a6845ed`  
		Last Modified: Fri, 21 Feb 2020 23:47:43 GMT  
		Size: 5.4 KB (5431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae58e099f730d41321cfbfe7799b177101caa4971fb689d5aa4a259b45532964`  
		Last Modified: Fri, 21 Feb 2020 23:51:54 GMT  
		Size: 258.7 MB (258698876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4524aa609acb8eff7f79b9aef1b1eb40f28b3e434f9d3f352dfb8ba5b4e06e87`  
		Last Modified: Fri, 21 Feb 2020 23:51:11 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1b785f352e2755dd1965e2212b856cc2f7f4a4e9b2e449749f01020c081242`  
		Last Modified: Fri, 21 Feb 2020 23:52:57 GMT  
		Size: 293.8 MB (293803546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
