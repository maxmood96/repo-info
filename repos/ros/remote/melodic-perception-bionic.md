## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:887a3f130bad35fb18466e468060392fc03f611809b8737df0812bdb7bbf4942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:34101d532e05e5b9363bb29e27e1cc7fbf53c0254d2341b03ca60df26d2f66fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742367409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea74d6b1bdcc793887121e6396df67ff0796b0cc0362ff8156643d5cfbc2c87`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 11:10:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:38:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:38:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 12:38:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 12:38:18 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 12:38:18 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 12:38:19 GMT
ENV ROS_DISTRO=melodic
# Fri, 26 Mar 2021 12:42:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:42:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 26 Mar 2021 12:42:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 12:42:27 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 12:43:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:43:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 12:44:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:51:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa0eff1a96d1d945845cab86a8e978cc925e0c70eb0c4c23df2d989f3d08c6`  
		Last Modified: Fri, 26 Mar 2021 11:40:20 GMT  
		Size: 840.2 KB (840161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c35c871baa65cb3164cc6ebb22d25b6b58e98c1eb7a2e9f8aaa302c71730643`  
		Last Modified: Fri, 26 Mar 2021 13:34:06 GMT  
		Size: 4.9 MB (4871708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eceba2cf9f62d789d7d061842ed0f7e0a057fe97bb23b64fb5407a0fbeb4cd8`  
		Last Modified: Fri, 26 Mar 2021 13:34:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d979e101411970ddb8cba4384d184bcd87ff97831750b093394ea1e1281d10fb`  
		Last Modified: Fri, 26 Mar 2021 13:34:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699aa13919017e86751e03729e28ca3fbbfd16d1c09647fcfe75aba194df35f`  
		Last Modified: Fri, 26 Mar 2021 13:34:53 GMT  
		Size: 259.4 MB (259395601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b160405461bb2f9411ae4c781b3368d5cdb43dae87ac27161c069b1a5ffef2a`  
		Last Modified: Fri, 26 Mar 2021 13:34:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e4fd40af4ab848d15bd361a02bc9fad70e1af6a482f3f34354e9fedb10b42c`  
		Last Modified: Fri, 26 Mar 2021 13:35:23 GMT  
		Size: 70.2 MB (70219845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a484de1813fcffae1bfac2b1fd3173fcbb64c069b962da3ecd33c30c92a1e1`  
		Last Modified: Fri, 26 Mar 2021 13:35:11 GMT  
		Size: 249.7 KB (249694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152603947cb77bc1508b568f31030d860e45f2dcb708db77538ddda3e7750ad4`  
		Last Modified: Fri, 26 Mar 2021 13:35:28 GMT  
		Size: 75.0 MB (74993187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0517b9e9db3f24fea6dd04c2a3bba70cd0c4383f36bea13e0540774d8b77349`  
		Last Modified: Fri, 26 Mar 2021 13:37:00 GMT  
		Size: 305.1 MB (305083556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:b786e8883a4f731e6ae77f970d282e8c4faff2d20c58a7122018a710df8c37c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.6 MB (645589339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fc0e264518ea8e7a2de24c3131b36a3ed35bd15a3f7e8530827809317acf54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 09:13:19 GMT
ADD file:474c32464fde8c7d9e10b46057ab5cc2e1fc203fd8677ea3640c631f85117888 in / 
# Fri, 26 Mar 2021 09:13:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 26 Mar 2021 09:13:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 26 Mar 2021 09:13:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 26 Mar 2021 09:13:36 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:03:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:03:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:03:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:04:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 14:04:02 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 14:04:03 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 14:04:05 GMT
ENV ROS_DISTRO=melodic
# Fri, 26 Mar 2021 14:08:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:08:12 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 26 Mar 2021 14:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:08:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:09:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:09:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:11:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:998199bcf9ef936a7f908e13358322e3ceff3224a4b18ade78181654c80572f9`  
		Last Modified: Fri, 26 Mar 2021 09:16:25 GMT  
		Size: 22.3 MB (22291239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b21c25a7bc95d706d25e4db24b7330a082cd700618204b85569a04519e8498`  
		Last Modified: Fri, 26 Mar 2021 09:16:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a6e767920e1c47edc24001be388f7332ecb232abb204adfe5163baa1db64b`  
		Last Modified: Fri, 26 Mar 2021 09:16:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f739a69aad0312ff68f8b450af0b4a076cee88dfea995283a79928b9d574ef28`  
		Last Modified: Fri, 26 Mar 2021 14:49:49 GMT  
		Size: 841.2 KB (841170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1eb8b50942c458929fd4f04670c58019e677dae4b21d8057f63147a50b80bc`  
		Last Modified: Fri, 26 Mar 2021 14:49:45 GMT  
		Size: 4.1 MB (4085629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcb68acffef6ac858782dd1dc8ad3c0c6ff543858974beddf91d9fc01ae520b`  
		Last Modified: Fri, 26 Mar 2021 14:49:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e640505ea96087687f5551261439a9bf80d5a047e707e9681cf902bccc92fa`  
		Last Modified: Fri, 26 Mar 2021 14:49:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8a03bf0e8ab0b3d9119220d0fdd57133649eab0af6f2a22e4ad42b6cb9a0eb`  
		Last Modified: Fri, 26 Mar 2021 14:52:11 GMT  
		Size: 238.9 MB (238862735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c9c7093574551a06622440adee9af96a3b0f3d22b9db2f24fe31a8db9efa7`  
		Last Modified: Fri, 26 Mar 2021 14:49:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed546e77e7fadc9517735e954c70b14b71b29b8f3129c5437af32eea01aea2c`  
		Last Modified: Fri, 26 Mar 2021 14:52:46 GMT  
		Size: 54.7 MB (54689067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d09db36b590a284b4fc5fe92e3f2cae2413ba017400990bb4cb3c82078122`  
		Last Modified: Fri, 26 Mar 2021 14:52:25 GMT  
		Size: 249.7 KB (249743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682056bd7b7c758ecb00b0e04ec35cd15d3f58d920cf2e1736324197e6205e76`  
		Last Modified: Fri, 26 Mar 2021 14:53:11 GMT  
		Size: 64.7 MB (64744843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f93339e21000f7010c1f4602b2f528eb89beab845c5315a8fb82923782987a`  
		Last Modified: Fri, 26 Mar 2021 14:55:35 GMT  
		Size: 259.8 MB (259822034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1395ae894485880d128ad640ec37e5c35c637475bcddf30bb6016a451a78ccb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.3 MB (703297506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf3b2d385a7cce8bf1a81916f1863b966143eb32927ffb26d54a2f29e18de34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:32:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:32:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:32:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:32:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 14:32:40 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 14:32:42 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 14:32:44 GMT
ENV ROS_DISTRO=melodic
# Fri, 26 Mar 2021 14:35:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:36:02 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 26 Mar 2021 14:36:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:36:04 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:36:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:37:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:38:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088a5fdb71356345c9275386f82ff5adfe26259ac6a250dbb4044a6fdc0019a`  
		Last Modified: Fri, 26 Mar 2021 15:23:30 GMT  
		Size: 841.0 KB (841011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba42aa30b8246822d07c12b6e55f270f35d86257ef50ec34e1b9f02b34c4fbe`  
		Last Modified: Fri, 26 Mar 2021 15:23:27 GMT  
		Size: 4.5 MB (4453640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16613bcbb5a5d178bd2e6f3ee319ecef39d93cedb20e518169ad503abed5a60e`  
		Last Modified: Fri, 26 Mar 2021 15:23:25 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d77aff4d7a66ea3c411615da2944506981909f6ca039c0fd604ce45199c83df`  
		Last Modified: Fri, 26 Mar 2021 15:23:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e7cb073f9a6dd180c645cb3a2c18886217c12eaa54a28094053c1ce799b96b`  
		Last Modified: Fri, 26 Mar 2021 15:24:36 GMT  
		Size: 252.3 MB (252316920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f35434c773ffcdf9d983cacd2a62d6b6c15baf3e78aeaf6c61b99fba5de3829`  
		Last Modified: Fri, 26 Mar 2021 15:23:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ee776cd8655d523d806f0e604220f2121643cf1e6d4e4a7f6639968e795dd0`  
		Last Modified: Fri, 26 Mar 2021 15:24:59 GMT  
		Size: 63.0 MB (63046885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15285202a5bd27d99146653ec631a690b5ac53ca827e5de78cc499e62248586`  
		Last Modified: Fri, 26 Mar 2021 15:24:44 GMT  
		Size: 249.7 KB (249691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446e8ded6416d485266a72edd8ff270c64d0f88dfc34aa3959d8dd036590d17d`  
		Last Modified: Fri, 26 Mar 2021 15:25:21 GMT  
		Size: 67.2 MB (67224312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f3a012105a036d19a12632befa0cbd1d669824b8e1694d10295dd3fb2361d1`  
		Last Modified: Fri, 26 Mar 2021 15:27:15 GMT  
		Size: 291.4 MB (291429378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
