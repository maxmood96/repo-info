## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:18bbd89d830184809fd9492381301acca9dcc7ecd3078d3b8c4b1b94ee43c694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:930424c2a01d59f52456a2678e529843529355c549067f30c6021b719becbed1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.7 MB (546662441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d139eb88f6cbb8bd25fbd4013c7522ce10453413cfc7b873a7f47dce9a1007a8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:03:50 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:03:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:03:51 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:03:51 GMT
CMD ["gzserver"]
# Sat, 24 Apr 2021 00:05:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f475d88930aab6fd2bc423304e95eb6f4986e4361e074070ba551f702f5ab2e`  
		Last Modified: Sat, 24 Apr 2021 00:19:31 GMT  
		Size: 235.1 MB (235133116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a928237d4f0f84c1e386b53ce4054080816dccd327881244f9bd349d49bc561`  
		Last Modified: Sat, 24 Apr 2021 00:19:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f17aac8491b5c3994de1bbc49604367bfc06912bb576e3ce5ba5665f5db38a`  
		Last Modified: Sat, 24 Apr 2021 00:20:23 GMT  
		Size: 269.3 MB (269279952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
