## `ros:galactic`

```console
$ docker pull ros@sha256:74aa252f955e70bb03f4451cfbdda76f6417f6730d467ff8521ccfeab7cd5826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:9d255be9195c6af4389d1c15c9f48352b2c7294a0fcb8d29ad23a9dceac16ad7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227752863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd420418598002fe81b21d57be99cd8ee9a01f4858b3d8fbabcc360bd7896ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 01:53:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 24 Apr 2021 01:53:52 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 01:53:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 27 May 2021 00:00:41 GMT
ENV ROS_DISTRO=galactic
# Thu, 27 May 2021 00:02:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:02:46 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 27 May 2021 00:02:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 27 May 2021 00:02:47 GMT
CMD ["bash"]
# Thu, 27 May 2021 00:03:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:03:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 27 May 2021 00:04:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 27 May 2021 00:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fbc9697fb73e1f55467886a56de4ed73ea1fa95a907d4eaa7cc7795c3f4438`  
		Last Modified: Sat, 24 Apr 2021 02:08:15 GMT  
		Size: 5.5 MB (5548747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a95aef5c90fc3ad3fbdf62df2fe49070101223c648c5648548adffb4b1602`  
		Last Modified: Sat, 24 Apr 2021 02:08:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175c1d7cad2105828be8f307599a3ccf1e81d1be86a72ca321e46e645a608b81`  
		Last Modified: Sat, 24 Apr 2021 02:15:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4089a7b633ad7bc0bb99c80369182dfcb19580550824a8608977656b6f243190`  
		Last Modified: Thu, 27 May 2021 00:08:47 GMT  
		Size: 103.6 MB (103595675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3392103b864b1fc30299d95d9fda8b132bfe7da42e7e3efa0b1229f32634453`  
		Last Modified: Thu, 27 May 2021 00:08:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cac9a1784bf2c87aa220b68788a50b24d24e784efecb2eacebb03e18f5f914`  
		Last Modified: Thu, 27 May 2021 00:09:11 GMT  
		Size: 66.6 MB (66551527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5bab54ffa87aacbd305a4d90cdadda9a7d4ddf203d9a2909e0061b8cd0e20`  
		Last Modified: Thu, 27 May 2021 00:08:59 GMT  
		Size: 230.5 KB (230548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e68e0c16a70443037eb61ffdf0b386fd68b62a676961199450234f753b60975`  
		Last Modified: Thu, 27 May 2021 00:08:59 GMT  
		Size: 2.0 KB (2030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0e5e858e69ef9c0a4e9f95f0e823a4bb75ae50b8b65c1ced62db5090aba04d`  
		Last Modified: Thu, 27 May 2021 00:09:03 GMT  
		Size: 22.1 MB (22098319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
