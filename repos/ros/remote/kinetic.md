## `ros:kinetic`

```console
$ docker pull ros@sha256:9f71d0a3155a840ecf6c9c2f7f79224ee3d3fe59f60a408c1adc5020006b2785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic` - linux; amd64

```console
$ docker pull ros@sha256:328ca8346b5d8366685b1061ceb959a40bf28e1db45e39b420a528c7ac7ba65d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385369213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c20092b18eddd2fcf94eebf33e24ce011760caf804eee41217f36d9067dda04`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 01:22:53 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 01:22:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 Nov 2019 01:22:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 Nov 2019 01:23:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 01:23:34 GMT
ENV LANG=C.UTF-8
# Wed, 27 Nov 2019 01:23:34 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 Nov 2019 01:23:42 GMT
RUN rosdep init     && rosdep update
# Wed, 27 Nov 2019 01:23:42 GMT
ENV ROS_DISTRO=kinetic
# Wed, 27 Nov 2019 01:24:51 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 01:24:52 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 Nov 2019 01:24:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 Nov 2019 01:24:53 GMT
CMD ["bash"]
# Wed, 27 Nov 2019 01:26:00 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2413f0bed0a66209ed901246e8f151ba518e4eb1b3717303e00875df171b1849`  
		Last Modified: Wed, 27 Nov 2019 01:31:00 GMT  
		Size: 6.9 MB (6937889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e0c2ce6f0e60388ac30ab3ef602ab2c5d08198ed68d3e31493eb6988e0cc5c`  
		Last Modified: Wed, 27 Nov 2019 01:30:58 GMT  
		Size: 13.1 KB (13102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df74e531bbd7e8c79e58e585334eadd9373789999db201d52c0e860943c0d3af`  
		Last Modified: Wed, 27 Nov 2019 01:30:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9251e3530954074e36ff8e50c883310a9605499d1916764b3c822fedea5c58f3`  
		Last Modified: Wed, 27 Nov 2019 01:31:14 GMT  
		Size: 54.8 MB (54770079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff08d617d661fe4f2c1b1ae7689a76647297e9bde6b1fe2d816a0f4a0c18aa1`  
		Last Modified: Wed, 27 Nov 2019 01:30:57 GMT  
		Size: 443.6 KB (443566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c1a5ab74dd08973c5069b70883e6fd13e4768aa015cd974ef8f30ef39e0179`  
		Last Modified: Wed, 27 Nov 2019 01:31:40 GMT  
		Size: 193.5 MB (193540826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94430f6a50379155ae297c72319861669ef978a8e555187a7393f78df72dc937`  
		Last Modified: Wed, 27 Nov 2019 01:30:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4cee62902b4ac893136b72c59d7ddca9bd5e6ed8df55a25f49bd207cd36bb7`  
		Last Modified: Wed, 27 Nov 2019 01:32:03 GMT  
		Size: 85.5 MB (85516413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:883106104357072e4011916e99987243b724d24ef59237c780d365dc3b9d7c9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336647680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46c93cd10743885e0475a762078bed4e9d0b46679b0faf540c74c4a3de7dfc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b4f2d68c4c3aabc6b84fd664c9d4e1e67fefdd0ff74664f4f4def3189bd39214
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350479932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64b8b9e62ca477d70be1b352d32154f88f1388531eb28c7c6977a700d11aef5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:09:39 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:09:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 Nov 2019 00:09:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 Nov 2019 00:12:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:12:14 GMT
ENV LANG=C.UTF-8
# Wed, 27 Nov 2019 00:12:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 Nov 2019 00:12:34 GMT
RUN rosdep init     && rosdep update
# Wed, 27 Nov 2019 00:12:38 GMT
ENV ROS_DISTRO=kinetic
# Wed, 27 Nov 2019 00:16:48 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:16:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 Nov 2019 00:16:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 Nov 2019 00:16:59 GMT
CMD ["bash"]
# Wed, 27 Nov 2019 00:19:11 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a010fc32571eae58db96ec75550ce02b64e5d668d2accf9fba61c66e29106aba`  
		Last Modified: Wed, 27 Nov 2019 00:26:20 GMT  
		Size: 6.0 MB (5959917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d247f84b81e76863e84635db36f3f0ec170dabb228e322975d435018941fb111`  
		Last Modified: Wed, 27 Nov 2019 00:26:18 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504965e33d884c9027cab5b4e3f5a0acbb234137ea604809f65454cb52f0fce4`  
		Last Modified: Wed, 27 Nov 2019 00:26:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29294b72a432ab1b558e8df5791bfed0abea8cedfebd340ba45f5c8bd81a9542`  
		Last Modified: Wed, 27 Nov 2019 00:26:34 GMT  
		Size: 52.1 MB (52066045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5c0bdce2fc2ce88f1350fc9c76be4f730229c3c1e5e83d714d75bb7a98ccb1`  
		Last Modified: Wed, 27 Nov 2019 00:26:16 GMT  
		Size: 443.6 KB (443608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39d0df7ab7054f595aed83edeb45da6e20201484f80a1e7999adc630a3d3458`  
		Last Modified: Wed, 27 Nov 2019 00:27:08 GMT  
		Size: 174.2 MB (174225018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cca73b15bab541593b51667aec9e966277dec7b283b47dfe2332381af7f80c`  
		Last Modified: Wed, 27 Nov 2019 00:26:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bf95fa418a228fdcdfe262d1718d24977c587c9874a7c95d0dc26f1686b63b`  
		Last Modified: Wed, 27 Nov 2019 00:27:38 GMT  
		Size: 77.8 MB (77818751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
