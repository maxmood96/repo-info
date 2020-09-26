## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:403fc929ea035b1063e6436dbcf02de8f4518e5b0bce98338d8385c00758c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:c27740dc93808d4644af7bebcc8fe0ddca92be1d3dbe2f533d3b1e86a115a560
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.5 MB (418497387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60a3d1963d419b15a9f23da630d35553668b728eadfb2f0da58fac7b5029b2d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:24:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:24:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:45:28 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 01:45:29 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 01:45:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 01:45:29 GMT
ENV ROS_DISTRO=dashing
# Thu, 17 Sep 2020 01:47:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:47:26 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 01:47:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 01:47:27 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 01:48:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:48:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 01:48:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Sep 2020 01:48:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:48:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:48:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 01:48:52 GMT
ENV ROS1_DISTRO=melodic
# Thu, 17 Sep 2020 01:48:52 GMT
ENV ROS2_DISTRO=dashing
# Thu, 17 Sep 2020 01:50:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.9-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:50:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:51:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:51:04 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff46beebaffa079e954504803bc595a5f6e147a355f4dedc87f40f3af82541e6`  
		Last Modified: Thu, 17 Sep 2020 02:05:15 GMT  
		Size: 4.9 MB (4868515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8f0e50c7d585ec379b79811c18fe858d1c056ff843ad99f5b83185707ea2c0`  
		Last Modified: Thu, 17 Sep 2020 02:05:14 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de63688b11552e31a081677d4f8cdec5298a10ec1d6aa5b1ddc9fb8b9e9aac3`  
		Last Modified: Thu, 17 Sep 2020 02:11:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee77e9c3f7390e8cc1b3e5e1fbfe31f13ad9e2af574a69d8b8abefbd9e7e0ac`  
		Last Modified: Thu, 17 Sep 2020 02:11:55 GMT  
		Size: 179.4 MB (179393476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f961fabbceff1d76e4305b1c6048337be354232737f97ccd151276da74f26e7`  
		Last Modified: Thu, 17 Sep 2020 02:11:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9cb2d87933e49c15eeeebe32d39cd5e8dcf84963da147f357cacaed4ff6096`  
		Last Modified: Thu, 17 Sep 2020 02:12:16 GMT  
		Size: 64.1 MB (64125632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b583f79a0bd0565b8b23d96cfbf1d02d4877720a5fe96e0ff0505fe881e2fc`  
		Last Modified: Thu, 17 Sep 2020 02:12:05 GMT  
		Size: 189.5 KB (189520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d334f1291e00addae04dcd53dbe2a5b6a7c2e0589390f526ccdebe2c85ee1b65`  
		Last Modified: Thu, 17 Sep 2020 02:12:05 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941cb035e0528e898f5053d856fdbabf27a3984d99d316fed7180889d0931ae`  
		Last Modified: Thu, 17 Sep 2020 02:12:06 GMT  
		Size: 4.3 MB (4312555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aac0a8fe3afab7b74ce7f8addcec2ee8736eaaeed13921b5704b49dd9e9668`  
		Last Modified: Thu, 17 Sep 2020 02:12:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce8b747454ce7b1b1bbe98187ed8d8c14061402d21cf744ce9e50506ebdf399`  
		Last Modified: Thu, 17 Sep 2020 02:12:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f950a80d5ba21059662ec26fe3015180498990e745c4cc6256923aa4720bdc`  
		Last Modified: Thu, 17 Sep 2020 02:12:51 GMT  
		Size: 117.6 MB (117639063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4513a205d8118f0760826c4476cfbc0d674c287c6ca95915497fd2b113d2f2d2`  
		Last Modified: Thu, 17 Sep 2020 02:12:29 GMT  
		Size: 19.8 MB (19787027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2736739d35d3c9ae936f706f035c128c562a29978a7ffd5abba42a778ff593`  
		Last Modified: Thu, 17 Sep 2020 02:12:22 GMT  
		Size: 638.3 KB (638343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b3635037471e27585a66cbeef5680c2ea64ee7cee962cd201c8ad4ef4c91f0`  
		Last Modified: Thu, 17 Sep 2020 02:12:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:2d41316bdddf47bf0db3be9a11aa3c2ee4ecb458775d8bcaf3029a4c901032bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354660910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b7e2ae37b64ecc25116c54fed282306d54cab4b731e1d6792a92338d59f8e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 25 Sep 2020 23:04:32 GMT
ADD file:0ddc5fefae097a5be4c925fdfc09e4a637b74627a8981f0e6fb9890580adc875 in / 
# Fri, 25 Sep 2020 23:04:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:04:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:04:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:04:40 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:52:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:52:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:52:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Sep 2020 00:15:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 26 Sep 2020 00:15:05 GMT
ENV LANG=C.UTF-8
# Sat, 26 Sep 2020 00:15:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 26 Sep 2020 00:15:07 GMT
ENV ROS_DISTRO=dashing
# Sat, 26 Sep 2020 00:17:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:17:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 26 Sep 2020 00:17:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 26 Sep 2020 00:17:47 GMT
CMD ["bash"]
# Sat, 26 Sep 2020 00:20:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:20:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 26 Sep 2020 00:20:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 26 Sep 2020 00:21:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:23:20 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 26 Sep 2020 00:23:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 26 Sep 2020 00:23:39 GMT
ENV ROS1_DISTRO=melodic
# Sat, 26 Sep 2020 00:23:41 GMT
ENV ROS2_DISTRO=dashing
# Sat, 26 Sep 2020 00:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.9-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:27:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:27:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 00:27:23 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:20e126218ac644f56ef7147c3363108a0814d921e6016af54a1b4c964159f1a9`  
		Last Modified: Fri, 25 Sep 2020 23:06:39 GMT  
		Size: 22.3 MB (22279517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d156c2b31482935ec0363b6e3f1cb6fc56da57e61fc80078914918fe53f8fa5`  
		Last Modified: Fri, 25 Sep 2020 23:06:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1a0dbe2162972438aa89d4f90dca5db0e4cee58819ba354ea1c0031101b7a`  
		Last Modified: Fri, 25 Sep 2020 23:06:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb78937af11e41b8b67fc193c013f76d8597e2901f9207cb60bcc96c6494422`  
		Last Modified: Sat, 26 Sep 2020 00:43:43 GMT  
		Size: 838.9 KB (838879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bcc9cef45fa068e47d37c7bc183a512bea02bfcff3e7e007e458352c5a37ca`  
		Last Modified: Sat, 26 Sep 2020 00:43:42 GMT  
		Size: 4.1 MB (4085050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd428060fb74592076e296fd161a779da260ddd29b8f39ec36bfe7e0e4ef7ef`  
		Last Modified: Sat, 26 Sep 2020 00:43:41 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7422b314a6e26cdf55febdd3ab72288b5ddec15c283f99baee45ab2faa20a3`  
		Last Modified: Sat, 26 Sep 2020 00:52:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063bc9560c2a7e478463e6f04405ee2ea5cc2639905a834cbebe104ef5f7a136`  
		Last Modified: Sat, 26 Sep 2020 00:53:00 GMT  
		Size: 153.5 MB (153527444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6217869449fd4c684ceebc3248fc61506c4a10fb6529c672e82b07bd4f6b0791`  
		Last Modified: Sat, 26 Sep 2020 00:52:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc122089dd4749fa715c03527f166d340d1a9ba4500ef3ea8de8e3e50fd6f08`  
		Last Modified: Sat, 26 Sep 2020 00:53:21 GMT  
		Size: 48.5 MB (48528951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6247062a443176534f8de64a793d1c1d3e046ad24b5f54de243c4bfe3e8c8391`  
		Last Modified: Sat, 26 Sep 2020 00:53:08 GMT  
		Size: 189.9 KB (189936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7ed62f2b9cd3fcba149fbf92d0298723e11f21b2832ad4f49a2acaad4d7685`  
		Last Modified: Sat, 26 Sep 2020 00:53:08 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0a429e950da7a97f648a14b13db508ae0f5368e92da3390e64e598cf9be9c2`  
		Last Modified: Sat, 26 Sep 2020 00:53:11 GMT  
		Size: 3.2 MB (3248999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d28121b612100bbaf523da64df086e60cfebf0716a4a097c1a42a68beb7421`  
		Last Modified: Sat, 26 Sep 2020 00:53:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16de8ecdcdcbc7ccbf797ab5e104d20db99674a742fcd592a1022cb0a7e84053`  
		Last Modified: Sat, 26 Sep 2020 00:53:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e6ee48f566e1cfdd41ebe185e75262d0240f3490192e36e272b1659d9c3e9a`  
		Last Modified: Sat, 26 Sep 2020 00:54:10 GMT  
		Size: 110.5 MB (110520500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17fc034d3a616963087ee899161ae82c11b881839e1ae9a04ac0c5397df99e0`  
		Last Modified: Sat, 26 Sep 2020 00:53:35 GMT  
		Size: 10.8 MB (10801241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b39abb668b335f745dd21aecf22924ae981e8c405504dec0c4e189616775b77`  
		Last Modified: Sat, 26 Sep 2020 00:53:29 GMT  
		Size: 634.8 KB (634830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3d1243c1d8651b3536017ec7fc0d9985f11e0d265a93266fefcf8925302b8c`  
		Last Modified: Sat, 26 Sep 2020 00:53:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:92ab8bde434047bfb4d3938cbad9cd21edc0ef887098b013b08584841a4a527f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386982177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fb1585d97c7480d64d6a0e9a29af1b9825c755e288cd989aaea5ee067e4417`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:16:37 GMT
ADD file:9eedc88c2028d53a81210b52c98121dddea7e30ecfbd4d11d2a1b2bdc94a0102 in / 
# Wed, 16 Sep 2020 23:16:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:16:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:16:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:16:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:05:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:06:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:06:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:57:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 01:57:52 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 01:57:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 01:57:54 GMT
ENV ROS_DISTRO=dashing
# Thu, 17 Sep 2020 01:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:59:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 01:59:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 01:59:55 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 02:00:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:01:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 02:01:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Sep 2020 02:01:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:01:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:01:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 02:01:50 GMT
ENV ROS1_DISTRO=melodic
# Thu, 17 Sep 2020 02:01:51 GMT
ENV ROS2_DISTRO=dashing
# Thu, 17 Sep 2020 02:04:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.9-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:04:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:04:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:04:52 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:e2d8ee3976bc7c15c8a5279cdf0249b7e41b2a489771330d0f7affb26dd7acfb`  
		Last Modified: Fri, 04 Sep 2020 00:25:25 GMT  
		Size: 23.7 MB (23722305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007857f7b9b52d6efdfea9e086e6eaf35519130ff97bfe89970353f0ae53f13`  
		Last Modified: Wed, 16 Sep 2020 23:18:23 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43927e60f12d8b877ded6af5048b2ac5753fe78caba77a6bbbece4f98559b672`  
		Last Modified: Wed, 16 Sep 2020 23:18:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f935dc942a8d9dc0bd78fe8add3019f0bab77e12b5d1e093fc05245365a5269`  
		Last Modified: Thu, 17 Sep 2020 02:30:40 GMT  
		Size: 838.6 KB (838630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4283a4fa6c260073e1d499eabe4fd0ed4124cf7d66867a95e5e35f09b3d6e8f3`  
		Last Modified: Thu, 17 Sep 2020 02:30:35 GMT  
		Size: 4.5 MB (4451785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f58fc1ef9991757e1beb76f6b281bf95217cb7142f9a00ab899033ceb60ac6`  
		Last Modified: Thu, 17 Sep 2020 02:30:35 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b199c085c52fe0274c599b91d7c657727b30bf4a0afcd08a23c113569fb9f101`  
		Last Modified: Thu, 17 Sep 2020 02:42:58 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff1ecdb41fc83d0e21c6caaa1f34ba33298cba6cf74cc2af8f0ddb944bda179`  
		Last Modified: Thu, 17 Sep 2020 02:44:28 GMT  
		Size: 165.1 MB (165082373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff4905ba00c125a0dfa343d6ab972fe7cfea9688bc3f597b2fe4294dcb68f84`  
		Last Modified: Thu, 17 Sep 2020 02:42:58 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f897397a03348ebe319d7779cc5d53748a0a77035bde58cef8e738df3c0b30c`  
		Last Modified: Thu, 17 Sep 2020 02:44:54 GMT  
		Size: 56.8 MB (56838646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d8feab5a422ac53f013a5922138dfa0790166b710bbb2e14192273be904f94`  
		Last Modified: Thu, 17 Sep 2020 02:44:37 GMT  
		Size: 189.6 KB (189574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c4c1caeaea1c6784766e1eca1537ddd298bb6b3470648c1019b6927e7698ce`  
		Last Modified: Thu, 17 Sep 2020 02:44:37 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352de9586b40f8a89dc41a07638a6418981b561c558b1eb41303bc4310567cf`  
		Last Modified: Thu, 17 Sep 2020 02:44:40 GMT  
		Size: 3.7 MB (3664619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e47e648336642f9ed8b5e0e5fc83b2e84b538bf5646ae6b39887e7484f299a`  
		Last Modified: Thu, 17 Sep 2020 02:45:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71aa3ae116b9f6e889e823325bf1290e24a7b3bb0bef6580fcdf09d4346cc9`  
		Last Modified: Thu, 17 Sep 2020 02:45:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ae12c114c53cf30f72bd75bb836b2819d1544d18067f3cb1ce11c8c159c964`  
		Last Modified: Thu, 17 Sep 2020 02:46:30 GMT  
		Size: 116.6 MB (116611022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8480b1e3fcc4658bc58830d630c093d34a7f7bc71d6096c8fa71106b9ec5c6`  
		Last Modified: Thu, 17 Sep 2020 02:45:34 GMT  
		Size: 14.9 MB (14942107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735a20c85a1c7012a8ace079affaa5dc483addb18bcad23117d103f4e1f74221`  
		Last Modified: Thu, 17 Sep 2020 02:45:11 GMT  
		Size: 635.6 KB (635552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d2329cee3eda133aafa199240ddf6875e95c9cdc49924449bcdb610ec92a9`  
		Last Modified: Thu, 17 Sep 2020 02:45:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
