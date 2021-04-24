## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:a88348012ee79d7a266771a8054e7c52cd0dc6d6bd71e191cf9c498d292b6ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:17217e15fbb50a0873f3745d4902ca47a4bba8cdb13d5db0764efa89717dbde5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318254000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4ebc9b8cc646a267b606a9085691cc7ece1005d2bcba8b8e33837c7e0f37d0`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 24 Apr 2021 00:06:03 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:09:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:09:43 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:09:43 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:09:43 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:09:43 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84e3d913f988af95e954537fcffb78eb9c9c3d5b91f5cdcf02a1f1c932a6d5`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 16.2 MB (16150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47f933436cc57965cecdb865715bb01535d7aa664ecd5aaa38504b7d29a5a5`  
		Last Modified: Sat, 24 Apr 2021 00:20:34 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c28531c6ee3b84f26807ed129be1a1966692c7120ecfe5685853ca4d6a0873`  
		Last Modified: Sat, 24 Apr 2021 00:20:33 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8ad6644768422c5ad05afb901373b192e8b3b226361adb1d3b00e49afe5901`  
		Last Modified: Sat, 24 Apr 2021 00:21:10 GMT  
		Size: 272.4 MB (272372428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9815765b2ed56b325178f5b8015e18283270d5cce085d15a2ba4146a5df73c`  
		Last Modified: Sat, 24 Apr 2021 00:20:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
