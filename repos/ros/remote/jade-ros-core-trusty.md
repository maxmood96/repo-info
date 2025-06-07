## `ros:jade-ros-core-trusty`

```console
$ docker pull ros@sha256:8db22822d428f7197f97296e61d5eec0db7f98d45d1084f9b1abc77c6f83de35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `ros:jade-ros-core-trusty` - linux; amd64

```console
$ docker pull ros@sha256:eb055e086f512cdbf578acdf0edb71a4cc4d3b57144acf82826650d76730ed65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267258084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a36f90b1060367010a15548fa169e9e2867b229e68d8cb8c5d90f1def7123c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:40 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 25 Mar 2021 22:33:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=jade
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Fri, 13 Dec 2024 13:52:03 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Fri, 13 Dec 2024 14:33:56 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Fri, 13 Dec 2024 13:28:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7947e2e80596bd2dd6aa721c50543b02d859c18c479e6fee7974186341fbf`  
		Last Modified: Fri, 06 Jun 2025 22:50:20 GMT  
		Size: 14.0 MB (13999678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53493d080ac5b1dcf02f0544ab568f501bbd0cd25d5a3d4c090f79cfade15863`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b7382600e2675b92184b3c9e606962fb3a31d0fcc797c9718d86c5aeb77e1`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0540af077fd693d6d887b2c1377227d8aca763ac4abce016145113d53735c2`  
		Last Modified: Fri, 06 Jun 2025 22:50:21 GMT  
		Size: 30.9 MB (30903820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a90e857d50dc2639933dc58909049bb48dc5e49480f0b333cf30fd28555667d`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 1.9 MB (1907624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d6930123b937d48d4d52a308e963df7fcdc06810cc42be7feaafbc10e10241`  
		Last Modified: Fri, 06 Jun 2025 23:07:49 GMT  
		Size: 149.7 MB (149666410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a118e840e02939fac45745192b1b0256e7a176b68dd4d15b726e57f220d86`  
		Last Modified: Fri, 06 Jun 2025 22:50:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jade-ros-core-trusty` - unknown; unknown

```console
$ docker pull ros@sha256:99e86b38b85d899582e894c07cb748ad78c2bb83cac0936a1bd5216b3085d5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27880971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7395f48bc2956f8e14a7fa14a89c68b9a89735443df0d2e58fce33676304b66b`

```dockerfile
```

-	Layers:
	-	`sha256:346709e2a81f7106411d18212ab3b1201698f4c015531e078f657e347ed9f6d3`  
		Last Modified: Sat, 07 Jun 2025 01:21:36 GMT  
		Size: 27.9 MB (27861459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d082fb13a4d28711f424ca850417e78f648e37969242f6fbf68a19007e335637`  
		Last Modified: Sat, 07 Jun 2025 01:21:37 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jade-ros-core-trusty` - linux; arm variant v7

```console
$ docker pull ros@sha256:678e613baf82824842662f979352d9558f8b1b620d3a8e131ea2046df54e90a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244636129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1282658dc06965c6e405faf94148245361f15242cdff182d195c8270abd8898`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:07:46 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 25 Oct 2022 03:07:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 25 Oct 2022 03:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 25 Oct 2022 03:07:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 25 Oct 2022 03:07:49 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=jade
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Tue, 14 Jan 2025 21:10:21 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31831ce9fd9e38ad9d926286efdb85e400dc823da723d72cc676869c295fb0`  
		Last Modified: Sat, 14 Dec 2024 10:55:47 GMT  
		Size: 76.8 KB (76775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66373b79ee1bedb2a2bf237fb2a717660559ee8e3fec0aae52d9797c2b32b27c`  
		Last Modified: Tue, 14 Jan 2025 21:05:11 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca3ba35474a2e7add4548570538f01ba4e19ba476ef013e6894b61ee78fc57f`  
		Last Modified: Fri, 06 Jun 2025 22:52:08 GMT  
		Size: 12.4 MB (12355346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3a1499d5668b6eeb89a9466248af62e9ca582a05b6194ab6e3d02eee5dc26e`  
		Last Modified: Fri, 06 Jun 2025 22:55:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8938a18f64a189658ee8f48b5e9f7a626ff41fcf30c5f874cb2abb63d68ef65f`  
		Last Modified: Fri, 06 Jun 2025 22:55:37 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263cbdaf4bc7d3a241568d22257a71f9904927c34f31958e9158bce6ef124d42`  
		Last Modified: Fri, 06 Jun 2025 22:55:39 GMT  
		Size: 28.4 MB (28374521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a92fe5263a2bc487b090e21e20f621403dbf2bbe128fd8708aba520322cceda`  
		Last Modified: Fri, 06 Jun 2025 22:55:39 GMT  
		Size: 1.9 MB (1907400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e4d6c3244eb00fe78adf5d790629099bc764bb9edc1c0c19c2e6e30a138bfe`  
		Last Modified: Fri, 06 Jun 2025 22:55:14 GMT  
		Size: 137.3 MB (137281787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f438e1a65e86df020def93be8ab1a263a07888112d72daaf1891da6b229ace`  
		Last Modified: Fri, 06 Jun 2025 22:55:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jade-ros-core-trusty` - unknown; unknown

```console
$ docker pull ros@sha256:5472f8364c11380e038f52452906decd014c9fbc5239c6941368e70e6bb878bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27763204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f0a1fc6d9829e493f48659baa8b7f3d59232c949a3443cc639e8f52156b99e`

```dockerfile
```

-	Layers:
	-	`sha256:b53c64136a2dd2c67ff62bd15bdee26653485dbca1165181159a54a9eeec2a24`  
		Last Modified: Sat, 07 Jun 2025 01:22:02 GMT  
		Size: 27.7 MB (27743574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e738bea7bc26c0a9a66fbaa9e2e0edd52b2d23e7c03c55055b8242b6a3c24cc`  
		Last Modified: Sat, 07 Jun 2025 01:22:03 GMT  
		Size: 19.6 KB (19630 bytes)  
		MIME: application/vnd.in-toto+json
