## `ros:kinetic-robot-xenial`

```console
$ docker pull ros@sha256:f9e56daad437cc7b137b8d8a552d2e3520e30006bd07f2103607422f57aca959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot-xenial` - linux; amd64

```console
$ docker pull ros@sha256:bc03cca1ecfd253e18e6b62af3d0ca04d0fa8845ea2770a9887b086c5492e0c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379549708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e266071a92bf8e7ed2a9d06f4bb7933dd47a8f5da70c1cc35b32e906cd948c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:52:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:52:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 23:52:26 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 Aug 2020 23:52:26 GMT
ENV LANG=C.UTF-8
# Wed, 19 Aug 2020 23:52:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 Aug 2020 23:52:26 GMT
ENV ROS_DISTRO=kinetic
# Wed, 19 Aug 2020 23:54:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:54:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 Aug 2020 23:54:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 Aug 2020 23:54:35 GMT
CMD ["bash"]
# Wed, 19 Aug 2020 23:55:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:55:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 Aug 2020 23:56:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:56:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42671ddcc4761d1d5fda3befca1df0cff8f5b089a15ac8f25584718f7b30fcf`  
		Last Modified: Thu, 20 Aug 2020 00:36:26 GMT  
		Size: 5.4 MB (5362352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35866558c9e396905f6037ddcdfaa347f3cf2b8f0cb8f078a085e4f310ede188`  
		Last Modified: Thu, 20 Aug 2020 00:36:24 GMT  
		Size: 14.7 KB (14742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8221188695e539ec2da04dedd746404b841571bcbeda48393aef6cda24ac3382`  
		Last Modified: Thu, 20 Aug 2020 00:36:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdaf14b56f89f00c072a182ecb31c3d819ea5556a6a6153acb9849306b64f6f`  
		Last Modified: Thu, 20 Aug 2020 00:37:47 GMT  
		Size: 187.1 MB (187149202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5ed5057087c407b26c75cd7f1856ae6f3d7c09fce9cad0a28b23bf756b71bd`  
		Last Modified: Thu, 20 Aug 2020 00:36:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db246a84c2eb39369aef16425c7fd40e1c9c44ec3f49df2e97c51c31c380369`  
		Last Modified: Thu, 20 Aug 2020 00:38:04 GMT  
		Size: 57.2 MB (57240390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809e77f87840c7bd27dd40d9270985d96e55cfad7ccee6229078c6bdd265c4d`  
		Last Modified: Thu, 20 Aug 2020 00:37:52 GMT  
		Size: 262.8 KB (262827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cce60fdb58ce0f98b011103ae3fdd691f69046a7326604987e4840cc1a01a04`  
		Last Modified: Thu, 20 Aug 2020 00:38:07 GMT  
		Size: 63.6 MB (63572756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d27a3ebbea03e9e660773a903a6afc53ba76043280f81fc1fe5398a402b4cf9`  
		Last Modified: Thu, 20 Aug 2020 00:38:16 GMT  
		Size: 21.5 MB (21497925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:f518e76bfec11a764a9695a87e17b5aa408ff9655ea7a4da8da4d8193de363a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330602021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42d4371ce140965e901b249cb3d90aad113c161109e9c5bddd32eb65dc3769a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:46:44 GMT
ADD file:0b278cf0607b320084ec5b7202c2165582b90918197e7c7a3b6f5a978b67dac7 in / 
# Wed, 19 Aug 2020 21:46:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:46:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:46:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:46:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 22:29:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 Aug 2020 22:29:31 GMT
ENV LANG=C.UTF-8
# Wed, 19 Aug 2020 22:29:32 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 Aug 2020 22:29:33 GMT
ENV ROS_DISTRO=kinetic
# Wed, 19 Aug 2020 22:32:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:32:04 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 Aug 2020 22:32:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 Aug 2020 22:32:06 GMT
CMD ["bash"]
# Wed, 19 Aug 2020 22:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:33:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 Aug 2020 22:34:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2fb84101310d5621e3be19975c1bb24b9f684f7ffec110cb3d4982441c388a96`  
		Last Modified: Mon, 10 Aug 2020 14:27:50 GMT  
		Size: 39.0 MB (39047599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb62b8b664ef29d7c2413ebe2c638345e086b0c0519560854eae02c7e1c873bf`  
		Last Modified: Wed, 19 Aug 2020 21:47:57 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d891ce98e9b325ec87d26f9bb78ce486bb420846e496514de1af5e588b43404`  
		Last Modified: Wed, 19 Aug 2020 21:47:57 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361ed46998eb1705595b9fada81f47ab2ace3728bdd2f497680f5e8480b77530`  
		Last Modified: Wed, 19 Aug 2020 21:47:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9100dec9138b3098e55244cce8dc401d1b7dc0a5e6530daf3a78ef27c3322c9e`  
		Last Modified: Wed, 19 Aug 2020 23:15:27 GMT  
		Size: 4.6 MB (4615382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7b35d7dd6df61d7c29c9c48efafbe84bc9abb3e27af740040976a027ae5e5`  
		Last Modified: Wed, 19 Aug 2020 23:15:25 GMT  
		Size: 14.7 KB (14743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309e1fe0a6f12fe4fd6243e317127b78f852d62f0cb9893ef8826d30b2527ca1`  
		Last Modified: Wed, 19 Aug 2020 23:15:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c901563883e0c6209f4c05d161f953dd02bf08f2410a550fef06ef2634216c67`  
		Last Modified: Wed, 19 Aug 2020 23:16:22 GMT  
		Size: 168.0 MB (168009545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2ae779ec22740f850ccda71035491712275550dff2be9f7a24b8ab8c69c008`  
		Last Modified: Wed, 19 Aug 2020 23:15:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42656b198f53fb5cee1885331b56023d373c943f3be84cc1bef7fa854763f419`  
		Last Modified: Wed, 19 Aug 2020 23:16:41 GMT  
		Size: 42.9 MB (42892355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4b8a791f8a2b69215074add4a2a2eb949978df149fb36ba1041cdc0567b0c6`  
		Last Modified: Wed, 19 Aug 2020 23:16:29 GMT  
		Size: 262.8 KB (262848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef35062d493611d95eed66d1aca062dfd283a3bbe9878be1097de13d0214afab`  
		Last Modified: Wed, 19 Aug 2020 23:16:46 GMT  
		Size: 55.5 MB (55500384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d4c688cbfcf2dac7f335cf19a90cf14a4ec73345897a59c6f3e0f3836e33b7`  
		Last Modified: Wed, 19 Aug 2020 23:17:01 GMT  
		Size: 20.3 MB (20257208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:91d7fc74cd1195e02dd8f08dcfe9ecfabe7693e84206f6619b3caa2f52a89662
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344914473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dc99bf2b4941a6444db41f3066b4dcea6add9c453756b8269b9bf86076fb4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:31:42 GMT
ADD file:20ffb81d6b7edd3826c028369ed1774914394328d1ccef79ecee109f5cfbcc5f in / 
# Wed, 19 Aug 2020 21:31:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:31:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:31:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:31:52 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:04:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:04:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 23:04:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 Aug 2020 23:04:44 GMT
ENV LANG=C.UTF-8
# Wed, 19 Aug 2020 23:04:44 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 Aug 2020 23:04:45 GMT
ENV ROS_DISTRO=kinetic
# Wed, 19 Aug 2020 23:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:07:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 Aug 2020 23:07:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 Aug 2020 23:07:23 GMT
CMD ["bash"]
# Wed, 19 Aug 2020 23:08:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:08:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 Aug 2020 23:09:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:10:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3266c9b0302777bdc8ccdffab895ef058fb0777dc7600b0fe0b6c80dd3e71f9b`  
		Last Modified: Sat, 08 Aug 2020 00:25:28 GMT  
		Size: 40.1 MB (40073893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5240d1a89e17ed7dda51e3b38d3749e4ab3fb2fc2433de69ea23a838bb00c7`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be065fa7bcd4d9f2540e1fec00c455a04755974444b17fb108b73cd4b15963a1`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75305dc60d93c15276fd1b3dc21a09ef1ce9c248393c85eb1a5caf2be6e02671`  
		Last Modified: Wed, 19 Aug 2020 21:33:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237a19dac9380ba6ab00aa54052f33e6bb3bbe1c4a625e2ef22b31aa66529735`  
		Last Modified: Thu, 20 Aug 2020 00:01:29 GMT  
		Size: 4.8 MB (4820379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff3feff1aeb4bd2c963508cb72c0252474df7077791b0fb914e434f42306a2`  
		Last Modified: Thu, 20 Aug 2020 00:01:27 GMT  
		Size: 14.7 KB (14742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e35b981a90510b5d844c0eae9992bbb135bf69a5fe205ddae0fec5fd02ed20d`  
		Last Modified: Thu, 20 Aug 2020 00:01:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4074369f7e153d0934f49bbb465b71614c2cdc2c71af6195c4d4917ffc63473e`  
		Last Modified: Thu, 20 Aug 2020 00:03:08 GMT  
		Size: 176.0 MB (175985859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3c4745e6db25e3ed3fd886adb36c0cdb5b04ea82cfeb3b7e9842a225f6f8e8`  
		Last Modified: Thu, 20 Aug 2020 00:01:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d9fe1e901c099d17b789742b443241b30c0ba43e8f4a886ddb0ad89efe055c`  
		Last Modified: Thu, 20 Aug 2020 00:03:41 GMT  
		Size: 46.0 MB (45952999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a125f56e6e58e8e801014cd5a2693ebdec9b92dd074f1615e2c8d8057fed5f`  
		Last Modified: Thu, 20 Aug 2020 00:03:23 GMT  
		Size: 262.9 KB (262887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da62263466dd00fe47e9b6590c9e48a5cf540e1a7be4754ce90bfb7928a38a0b`  
		Last Modified: Thu, 20 Aug 2020 00:03:47 GMT  
		Size: 57.3 MB (57285361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29859c69bc1524b9e8c1baa460b22544ee95e7a7de8ddda9b4dc3ac8873e0343`  
		Last Modified: Thu, 20 Aug 2020 00:04:07 GMT  
		Size: 20.5 MB (20516443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
