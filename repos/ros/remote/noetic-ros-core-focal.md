## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:2cc83a7816b08929fdfd1ce037092ec50973bf0b099a752c7800c22971dccdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:4d1702f85828363b44313153b4d5d436f36c0b7bffde4311d741d0a7458487b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208364780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a649735740edb38045e5b12ad9c6449558192df534b463dd3ecd909ac76b28`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:51:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:49:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 00:49:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jul 2020 00:49:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 00:49:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 00:49:02 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jul 2020 00:51:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:51:10 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 07 Jul 2020 00:51:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jul 2020 00:51:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbd34696aad22f9a861bdae9aed1bc14aed3426d245147e55a759747acc2357`  
		Last Modified: Tue, 07 Jul 2020 00:03:20 GMT  
		Size: 1.2 MB (1175806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d44cae379b4797d812ed05b65c080aba6074d55e8d8b0b0c612b3923d9f5a`  
		Last Modified: Tue, 07 Jul 2020 01:21:06 GMT  
		Size: 5.5 MB (5549483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220c1b9e59cfca503e7910992752f72112d96b996c272d25c279bcbe31fb9210`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a4ba7e4fc497b4f1a0be7a446e50235b46dad5ccad278a3a8ee1cc40e891f2`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3553832b88c00e08e2838c2b9831cdd3d12abea4969df2f9170580e76d7b7a`  
		Last Modified: Tue, 07 Jul 2020 01:21:49 GMT  
		Size: 173.0 MB (173047564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af350ef5cb0c86ea4497ddb587024085e35048a6edae8416c61954111ed90ce`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8b06ed15caf5b233f5b08c96d9eec5dceb742cd8313ee269800d1b5bde554c2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186850042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195bbc76478e4719cb5cd76826c28b78e84ab1222ff7957ad1b3ebf8f30063cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 20:07:56 GMT
ADD file:ae06152ebc8f87c96acdafd81a83019a5d8eb72794de1681258068b2bb8e0a26 in / 
# Mon, 06 Jul 2020 20:08:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Jul 2020 08:03:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Jul 2020 08:04:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Jul 2020 08:04:15 GMT
CMD ["/bin/bash"]
# Thu, 23 Jul 2020 08:31:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 08:32:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 08:32:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Jul 2020 08:32:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Jul 2020 08:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jul 2020 08:32:46 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Jul 2020 08:32:48 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Jul 2020 08:35:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 08:35:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 23 Jul 2020 08:35:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Jul 2020 08:35:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a5e6eaf4bfe33a6b61d4c2284c6beb68336002b649ce502269dd304113ca8b13`  
		Last Modified: Mon, 06 Jul 2020 15:49:47 GMT  
		Size: 24.0 MB (24034277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce870b787348a32cc2f713931cf049283449e10fe091a4dc7486e9e437fc6e2`  
		Last Modified: Thu, 23 Jul 2020 08:05:24 GMT  
		Size: 32.3 KB (32340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620bf01298d6df5f80d65efbb4f1f9ffc6981510fb8f3b349b0042721a4b1ff8`  
		Last Modified: Thu, 23 Jul 2020 08:05:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce892844334fbee407385ccd77580896aefc7556ce279d1776e70d4f0a46f516`  
		Last Modified: Thu, 23 Jul 2020 08:05:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ab22e26c934682ce41b3a390a86e4888145e1b7e56ccb505a93ff3209a3c6`  
		Last Modified: Thu, 23 Jul 2020 08:43:47 GMT  
		Size: 1.2 MB (1176050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e30e40f9ef8c27c12df0205e7d1500cc1f600335099ef2a9eac4d5c0f645b1`  
		Last Modified: Thu, 23 Jul 2020 08:43:46 GMT  
		Size: 4.7 MB (4674293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4c98f57e33a028066f060adedac16280bd00c701145953c41f8f876ebe6b99`  
		Last Modified: Thu, 23 Jul 2020 08:43:45 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662a4c9b01acfa803a2217e88f2d948865ad62f44cafbe5e6e5142e5a818bce1`  
		Last Modified: Thu, 23 Jul 2020 08:43:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71f4242e4a731f7da8c74d83486ec72e2ef878dc4981cb39c4491b86c7414db`  
		Last Modified: Thu, 23 Jul 2020 08:44:42 GMT  
		Size: 156.9 MB (156930203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c60c025ee9c335d06a5fd9ca473d326b44691f6d129a38f556eaf03cb70094`  
		Last Modified: Thu, 23 Jul 2020 08:43:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4593c5281130a009a3aff7fca40fc273a92bfa99041c12de39177b6e2893c958
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201416531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f512de6a155cede79f2dbb84f7e6f8dfac5978d9901bb2b88a0054e460a27a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:37:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 06 Jul 2020 23:37:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 06 Jul 2020 23:37:29 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jul 2020 23:37:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 06 Jul 2020 23:37:30 GMT
ENV ROS_DISTRO=noetic
# Mon, 06 Jul 2020 23:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:39:49 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Mon, 06 Jul 2020 23:39:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 06 Jul 2020 23:39:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1ab16d904a1fdd0d8d3bf4378ba8091441f6fa4efc5f1a4cbb96007992418a`  
		Last Modified: Tue, 07 Jul 2020 00:27:10 GMT  
		Size: 1.2 MB (1175980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4459a6ff20458c1e9ddb61cde61a0a3767b97c675670463e46b4942817e63283`  
		Last Modified: Tue, 07 Jul 2020 00:27:09 GMT  
		Size: 5.5 MB (5516710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ce6ceb4dd155db7ff7ae84a01089eb66468a8907beeef35311a2dfecf5960`  
		Last Modified: Tue, 07 Jul 2020 00:27:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e38c7e306b521663dcedeb17b7d0a0a4305eb436fb67bd55c2decea7b59ff1`  
		Last Modified: Tue, 07 Jul 2020 00:27:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055015740252b376cd03adf98092083837a42ecec3bebdf2071a885790006097`  
		Last Modified: Tue, 07 Jul 2020 00:28:06 GMT  
		Size: 167.5 MB (167529240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2766dcb13a02fa22a925d84995c637f73c55a8c7f8de3ccc964685cd4416829`  
		Last Modified: Tue, 07 Jul 2020 00:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
