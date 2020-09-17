## `gazebo:libgazebo7-xenial`

```console
$ docker pull gazebo@sha256:ae79c9debc417b013ebc113d881aa56bb488728653bb672890deb6070b3dde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo7-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:b0fafa8e91ed8af3772fe61861403e4be1cafb47b4a512cc86f0bdccb08b15a0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482840274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ee0dfbe8c180f8bedf4c1f21e65bcf8d0a5d8c43c2a6717e63f77c39d47fce`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:22:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:22:01 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:22:02 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:22:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:22:02 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:24:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo7-dev=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ef38e9401109365596af8828ae7e9d9af506b5ff583b5873e267ea43b1780d`  
		Last Modified: Thu, 17 Sep 2020 00:44:22 GMT  
		Size: 181.6 MB (181636131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa14dd9f226b37ede587989373891badada90544df0dd15200bfcd5c18ea359d`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ab0250b87fc490d2cafa048d683db9a5d87c0f691d530bb68764c17c1b7a2`  
		Last Modified: Thu, 17 Sep 2020 00:45:18 GMT  
		Size: 240.4 MB (240416193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
