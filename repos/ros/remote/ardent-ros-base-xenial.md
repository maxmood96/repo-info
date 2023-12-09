## `ros:ardent-ros-base-xenial`

```console
$ docker pull ros@sha256:e90791d44e74f405b25bc332d1945b79586a3c6a5480b6ff9f4b1229faae4a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:ardent-ros-base-xenial` - linux; amd64

```console
$ docker pull ros@sha256:5c8fb19b2f60c98c270e03ff073d4c1eccf06302e27db03eb809b2a6fc1268e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332499143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55740d57064c5cdf16e932c325141ea7bbfb9da6f111a6d3220ea4f8a93b7749`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 03:36:08 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:36:09 GMT
RUN echo "deb http://snapshots.ros.org/ardent/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:36:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:37:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:37:15 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:37:15 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:37:41 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 03:37:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:37:49 GMT
RUN pip3 install -U     argcomplete
# Sat, 09 Dec 2023 03:37:49 GMT
ENV ROS_DISTRO=ardent
# Sat, 09 Dec 2023 03:38:38 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-core=0.4.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:38:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:38:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:38:39 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:39:59 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-base=0.4.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4476128daa02ed514e79ec829e0e7598f390cae00f3c700e5ea8c15d9be6c6f7`  
		Last Modified: Sat, 09 Dec 2023 04:45:07 GMT  
		Size: 129.1 MB (129126295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9ea2c11acdb298b38d52552fed59fd9841c29bfe0584ffff278ab93a24322`  
		Last Modified: Sat, 09 Dec 2023 04:44:49 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90de046ed7fd1be41e7e9b7864ab4f25c9c53b948040ccab320310d2b7098931`  
		Last Modified: Sat, 09 Dec 2023 04:44:48 GMT  
		Size: 17.0 KB (16979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1528acba51016aa0725cca15f962986e306367b34325caf5d68287c6996424b`  
		Last Modified: Sat, 09 Dec 2023 04:44:54 GMT  
		Size: 26.7 MB (26696070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b838fee1493f2d704ced48c03a333c24f24b13a5d47271cdbc255c7eb09642f`  
		Last Modified: Sat, 09 Dec 2023 04:44:47 GMT  
		Size: 1.7 MB (1679570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286450c54500bccfd3d3d2dea01141bea2aadac368fea3f1d940db65cd71a93e`  
		Last Modified: Sat, 09 Dec 2023 04:44:47 GMT  
		Size: 2.5 KB (2543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff2429ffc09d90bbb9e49afd4f9a9fe103dd80d343b9f6934bb44795d592676`  
		Last Modified: Sat, 09 Dec 2023 04:44:47 GMT  
		Size: 148.0 KB (147981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5f6ac3fcc98fd2410dc5bc584283d5cfe0e5e43cde392a3d5255399ba37cb0`  
		Last Modified: Sat, 09 Dec 2023 04:45:00 GMT  
		Size: 50.9 MB (50926939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec27fb513f27233241e9e620e2b8fad44d9e14f35a45361210d47f173c60a675`  
		Last Modified: Sat, 09 Dec 2023 04:44:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b393f2899ffbe35ea86894e283eec06af4a42f70cf1690381819bc9c62fd0b4f`  
		Last Modified: Sat, 09 Dec 2023 04:45:33 GMT  
		Size: 77.4 MB (77403234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:ardent-ros-base-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a82c1a90a27d86a6d35752760f337dcd6c23c7965dff043d3566be7d14b29a9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270118599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2f865c5d47e0f74288d69eb5bcfeb468fc275fcf27809e8fb900b5f350f3e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:17 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 25 Oct 2022 05:55:18 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 25 Oct 2022 05:55:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:55:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 25 Oct 2022 05:55:19 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 03:00:43 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:00:45 GMT
RUN echo "deb http://snapshots.ros.org/ardent/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:00:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:01:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:01:28 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:01:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:01:50 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 03:01:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:01:58 GMT
RUN pip3 install -U     argcomplete
# Sat, 09 Dec 2023 03:01:58 GMT
ENV ROS_DISTRO=ardent
# Sat, 09 Dec 2023 03:02:49 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-core=0.4.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:02:51 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:02:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:02:51 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:04:37 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-base=0.4.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66927c6d1d3d2e9321c4893f7f2105b7cd23dfb082853d97ec08f188e271e612`  
		Last Modified: Tue, 25 Oct 2022 05:57:02 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000560be91651dcbf476ebacb8bf1f1339694a3327f8e6da2519e0b29b33eb5d`  
		Last Modified: Tue, 25 Oct 2022 05:57:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225a0253717abdc2ee23ea211c1c439c93b84231ec0a4f1c74762a205ba7234`  
		Last Modified: Tue, 25 Oct 2022 05:57:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815274a1c833b221a127c9378c3da89a9eb93dac4d44b85b531a405761293c22`  
		Last Modified: Sat, 09 Dec 2023 04:00:56 GMT  
		Size: 77.1 MB (77076033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed66ecb4b8af9b9176b160c58b324074be333e4b210ce9bc6a236ddf4110af41`  
		Last Modified: Sat, 09 Dec 2023 04:00:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3640f528c7518ee208b78c6abb3d2bf4ef29b2cb22b9e6353538368b18fda7fe`  
		Last Modified: Sat, 09 Dec 2023 04:00:44 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c010941601a9e548a564e72b43b856bae17f8162e230c74d6454e20430d46e`  
		Last Modified: Sat, 09 Dec 2023 04:00:49 GMT  
		Size: 25.4 MB (25369675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad041ad44b8ad2f140f931614aa9e2cc6fa1704ca0a8c0ef648f6e5df3bf4e3`  
		Last Modified: Sat, 09 Dec 2023 04:00:42 GMT  
		Size: 1.7 MB (1679908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a196834d0b37fed34b0fb76bf51c10054b21f5b657dd35e6f115818235804210`  
		Last Modified: Sat, 09 Dec 2023 04:00:42 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41769056ce7c09a0deff03d1243fcaa11b4789b13b353faedeffd7a2b47d93b6`  
		Last Modified: Sat, 09 Dec 2023 04:00:42 GMT  
		Size: 148.0 KB (147960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a924a2e239fc71fd1177296f56283233a64fb8bf212478e4be16e8b45eac02`  
		Last Modified: Sat, 09 Dec 2023 04:00:54 GMT  
		Size: 49.3 MB (49309684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393df100a125a7686233c642182f63e13a0e721c855a38fb4ec370cbc1da1d26`  
		Last Modified: Sat, 09 Dec 2023 04:00:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87d1510cbd1249b16d3c8a81b868c7163d10d9b8f0e5906a1ea69da095210cd`  
		Last Modified: Sat, 09 Dec 2023 04:01:20 GMT  
		Size: 75.3 MB (75274630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
