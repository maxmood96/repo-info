## `gazebo:gzserver9-xenial`

```console
$ docker pull gazebo@sha256:0412cee182096d8e9900ea01fbee22749ed885ec1d3120c0087123c04d1a4e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:7d23632752eb0d1a5f5fdcd4a6994dd0f7ce3081201da757c96514889b0c45a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269029711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2109d787479456df884b00231e82698241ba2822f429b4202ae07b20c23b1f9`
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
# Thu, 17 Sep 2020 00:25:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:25:20 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:25:20 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:25:20 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:25:20 GMT
CMD ["gzserver"]
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
	-	`sha256:c0e205af1b54a73e841f21db3e7959a57e565068a91207e99bd0c2f4fa6c0e08`  
		Last Modified: Thu, 17 Sep 2020 00:45:53 GMT  
		Size: 208.2 MB (208241759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764ae8b7716bc1ea237bcb6e5d1b353df1f8ab62c8ea7752bf994665450ef6de`  
		Last Modified: Thu, 17 Sep 2020 00:45:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
