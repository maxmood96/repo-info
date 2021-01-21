## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:a2886a75036f33e81c830a5b6b92ea803575c40783981a9e30c7ea66de4adf9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:41dab3e664f364cfbe57a4e099f84fb64d244a99a58b34fe9f3e33dfda6dab26
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.2 MB (437214810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2a1bb27def96744a940c007b04a719066b7cfb4fb7431473f2d40d01b93f56`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:37:59 GMT
ADD file:ef36fee25b0bd1d99979ecb8d54b206cec33d4e8fd2232189f0d8e5ab9754798 in / 
# Thu, 21 Jan 2021 03:38:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:05 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:26:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:02:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 11:02:32 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:02:32 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:02:33 GMT
ENV ROS_DISTRO=melodic
# Thu, 21 Jan 2021 11:05:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:05:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 11:05:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:05:50 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 11:06:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:06:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 11:07:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d519e2592276828ca171d85e0532899cd4f98c70f5c697b45fa2e126e9f9fe49`  
		Last Modified: Thu, 21 Jan 2021 03:40:27 GMT  
		Size: 26.7 MB (26709716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d2dfcfa9cd230ed3c47defec2670d45081598c721dd85cafc34ea459f970e`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3afe92c540b778c64ca316d1e679d55d2d2e812e450f516a808ee591f0c3f77`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea992ddb93cee91b21cf19902eb7c0780191f8454157802d68fe834ad6c72d5`  
		Last Modified: Thu, 21 Jan 2021 08:49:44 GMT  
		Size: 840.0 KB (840038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe549b7120b83770f6772179d9e937e479567ac1297ed6808a3c029da14a498`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 4.9 MB (4870380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3148dcdae1e4da81fc90c6c4dc4ca6a3612c7176d9a53c61cf366eb77428c96`  
		Last Modified: Thu, 21 Jan 2021 11:44:39 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97022b250a6f8d2ce144f6af08d49d2315bc186f0aefe044b72b6221046660b5`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5f0e3dbbabad092e0eca391faecfd40a766ec66cfc52873b3e646c4b28624e`  
		Last Modified: Thu, 21 Jan 2021 11:45:31 GMT  
		Size: 259.3 MB (259348853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4861edf5d2c91e3cf3bbd7b66c900178c66707bf5eb9a9225846f17d457659`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1487fd48d9e8b625af56d96beaf411cd973b8abbfe2c99c62d70e2da49976f5f`  
		Last Modified: Thu, 21 Jan 2021 11:46:04 GMT  
		Size: 70.2 MB (70210490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66d4d7c21a40f83cefd470b534b90fb735be7cdf630aad736bab4064e094224`  
		Last Modified: Thu, 21 Jan 2021 11:45:49 GMT  
		Size: 244.7 KB (244730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69955244f09b3b422392c01e273ff9e6948a5e920b5b1b4c407e547c8da14ebf`  
		Last Modified: Thu, 21 Jan 2021 11:46:09 GMT  
		Size: 75.0 MB (74987751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:4bc9f074dad0da2ca40c71901352f29749581e4318ac6be0e7c435ff9a797844
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 MB (385751614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192d4c93742a6bb5a4509aa426ea144f8d3b49660cd9a35903f347ef4dfdc2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:15:18 GMT
ADD file:270f582b851314ab60dfbbc136c8e36ec44a11ecba1448403947ce72b0f9c06a in / 
# Thu, 21 Jan 2021 03:15:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:15:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:15:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:15:27 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:30:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:31:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 04:31:16 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:31:18 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:31:19 GMT
ENV ROS_DISTRO=melodic
# Thu, 21 Jan 2021 04:34:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:34:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 04:34:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 04:34:41 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 04:35:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 04:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d8bd15f2f6189f24e8f1b5dc573a293c963565ab012ca6a42e51a3023e72e7e`  
		Last Modified: Thu, 21 Jan 2021 03:18:06 GMT  
		Size: 22.3 MB (22291204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e961f21c7ea83c265a6de2897b8255e9e03cf1d39b74fb208b4ca936c6a53c5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b017766c8f695603aa5da2f534135bd1fbe253f667ef6faa77a77c66be9ba9f5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb7679849b59188f62bf017de9112158370c1d2eee07a8d614ba382cf612b62`  
		Last Modified: Thu, 21 Jan 2021 05:12:20 GMT  
		Size: 841.2 KB (841181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd1c8ec76e1cf5b551b2db58eb684cae7c4a3219c7175d85b4bf9ea4e5fe998`  
		Last Modified: Thu, 21 Jan 2021 05:12:19 GMT  
		Size: 4.1 MB (4085304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf27b43dde6748aae4a2d48a18d094192f874983a13d5046c161f02d3e11ab77`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3331cdb0247821fb1bee41928bad1bbc5ed592cc12bbf4231a4fc73d5fbc3668`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6e907b6a25c975ec7df5ea0e052e876a9240a0ba005ec9567f9cff4ec0bf76`  
		Last Modified: Thu, 21 Jan 2021 05:13:28 GMT  
		Size: 238.9 MB (238858209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c3aad0df547a9dbab2ff8eafc39fb1fb18ed1142b42ec2fe715364426040b2`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045fe81fe6a997f99b44f1309fab3bca03096d3ac72d32cc7305f56e28ba9d5`  
		Last Modified: Thu, 21 Jan 2021 05:13:55 GMT  
		Size: 54.7 MB (54685291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bed2ac9eafd52a3e8676e666162cb862f05128ea8a0ade7fb76ba57658e93bd`  
		Last Modified: Thu, 21 Jan 2021 05:13:40 GMT  
		Size: 244.8 KB (244755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e7c4382226442371dbc99bb4a624d5adf61ce51ece504aae8d03e7afed0ac`  
		Last Modified: Thu, 21 Jan 2021 05:14:01 GMT  
		Size: 64.7 MB (64742789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:49ad5b514cddf228ded9b917e63b5d733fae8d583b02624ba150fbd4dd71fe2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411836906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64324f031a9ce2688cfec53ecb009636618a07a1dbe7a086100124eed3ccaf7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:35:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:35:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:35:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 06:35:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 06:35:25 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 06:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 06:35:26 GMT
ENV ROS_DISTRO=melodic
# Thu, 21 Jan 2021 06:38:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:38:15 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 06:38:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 06:38:17 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 06:39:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:39:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 06:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75de3cb7cc851400a98b3f91be110991f7d3e5ef9e3362b2a1feaabe73b663eb`  
		Last Modified: Thu, 21 Jan 2021 07:25:58 GMT  
		Size: 840.9 KB (840945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d872ef396f747e28f1e5d655b4da63120065e5b8c19b451d0fd13ff642a0b99`  
		Last Modified: Thu, 21 Jan 2021 07:25:55 GMT  
		Size: 4.5 MB (4453230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4f3dc2dc6bc64630a22a47f207e4ff99ae9332e157017224e77646d47bfe94`  
		Last Modified: Thu, 21 Jan 2021 07:25:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057714468f562896d1c4e3627158773a60491808b659912135a32dca69ad9b7a`  
		Last Modified: Thu, 21 Jan 2021 07:25:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103e24b70f294082f2960550a0eb380d50c9f603444376d7ae817a6817979c6b`  
		Last Modified: Thu, 21 Jan 2021 07:26:57 GMT  
		Size: 252.3 MB (252291599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4516c7021fd4f1b8f0e88498b2e05fa078217196d44328f57c60553902886c`  
		Last Modified: Thu, 21 Jan 2021 07:25:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2575f84475e6942fee5d8abfb64a779b1f0a9fdd2e7ad70431e56d5b245200ef`  
		Last Modified: Thu, 21 Jan 2021 07:27:24 GMT  
		Size: 63.0 MB (63046800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4b0fe1d8a028d051c12cfaa547ad557fc6a6f1b1e3940983fbe8b91fa28c4c`  
		Last Modified: Thu, 21 Jan 2021 07:27:10 GMT  
		Size: 244.8 KB (244778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfdd778eebf6fad9bf0d7419e206d80d7e56479fc61ff9443f13dc1b04d6a32`  
		Last Modified: Thu, 21 Jan 2021 07:27:30 GMT  
		Size: 67.2 MB (67224031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
