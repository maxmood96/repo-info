## `ros:melodic-perception-stretch`

```console
$ docker pull ros@sha256:b5159c8bf1df0ab748fa12e6dcb365704bdb59a65d11d64e6e4d424f50ff62ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-perception-stretch` - linux; amd64

```console
$ docker pull ros@sha256:c13e032c1ff4964a01829cd319602fc7b7787139722cec46ebba2443a0af53e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **882.0 MB (882033824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1433d9b80694d9dc8825f87bef7f3189cf236b553be2b90384624d52ea06b81`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 13:30:59 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 13:31:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Mar 2020 13:31:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Mar 2020 13:31:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 13:31:42 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 13:31:42 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Mar 2020 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Mar 2020 13:31:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Mar 2020 13:33:45 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 13:33:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Mar 2020 13:33:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Mar 2020 13:33:48 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 13:34:46 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 13:38:28 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ef9fe835ba4097929a9fec6ec52fd43d50941808f55952b707f6248bde37b0`  
		Last Modified: Tue, 31 Mar 2020 13:39:32 GMT  
		Size: 10.5 MB (10476681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379aaa17416bedf715c94b175e2f742897c65e8ee917822e1eafca2962e558e`  
		Last Modified: Tue, 31 Mar 2020 13:39:28 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a674fc9e0a46c773ff9c026bd20911d7bbfd32c9fb5463acc59890fc46985fe7`  
		Last Modified: Tue, 31 Mar 2020 13:39:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86905bfa0f3df6f3e2ee212ea77774f1da21364d9421e60255c696ba3f027442`  
		Last Modified: Tue, 31 Mar 2020 13:40:02 GMT  
		Size: 64.8 MB (64769273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531d8767f23d53bd6abf95d9ebe06b06c2baef35717392b041ab6f7fb621363`  
		Last Modified: Tue, 31 Mar 2020 13:39:27 GMT  
		Size: 439.9 KB (439900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e37a9f9829349400ae82bf296f05e5f0103f1af68864e2ab2136a142808397`  
		Last Modified: Tue, 31 Mar 2020 13:40:49 GMT  
		Size: 276.2 MB (276208544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeda344463a8910cf521a6ef8818b59cdb2df1bcbd615a36e0b5b917479908b`  
		Last Modified: Tue, 31 Mar 2020 13:39:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1ed1c083fd538c120a034a1a290645bfae65afe726e02ab2e00c98354efac9`  
		Last Modified: Tue, 31 Mar 2020 13:41:20 GMT  
		Size: 108.5 MB (108476123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ce83b44b201ae0f51b63e7d67d1278f09c57c3108dc2fe4d01a73180454fdc`  
		Last Modified: Tue, 31 Mar 2020 13:42:54 GMT  
		Size: 376.3 MB (376285558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:23b13a8bee7d417347801e4667573b859e9dcc810a3b348c6bf533d5f20fce59
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **799.9 MB (799893109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbde9b8cbef45183088636f762a97509d027acb3a0e8d3b800e7ec03005acd5e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:50:19 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:50:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Mar 2020 08:50:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Mar 2020 08:51:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:51:56 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 08:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Mar 2020 08:52:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Mar 2020 08:52:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Mar 2020 08:55:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:55:32 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Mar 2020 08:55:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Mar 2020 08:55:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 08:56:58 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 09:04:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffb04892983b197ec2012ff1e5f489d298a3d1e097fd400e600d9f5ba5b696`  
		Last Modified: Tue, 31 Mar 2020 09:05:05 GMT  
		Size: 9.8 MB (9774723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6b8b721a085eab12f64779dec536ba34ac8f16dd1717c52ef7b9c274c7dcec`  
		Last Modified: Tue, 31 Mar 2020 09:05:02 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a13c4ba112de5fca316200409698b68af67bb359c22880fedb9f0c978529dae`  
		Last Modified: Tue, 31 Mar 2020 09:05:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ce74e2e465788ad2b3705897a2121bdf9917d0c435e7fdda3fbf0ff46e225`  
		Last Modified: Tue, 31 Mar 2020 09:05:18 GMT  
		Size: 62.1 MB (62092992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1d9278a758d83e399e2983b086d9bb98a57834e9baab02613f2bf95d5eca06`  
		Last Modified: Tue, 31 Mar 2020 09:05:01 GMT  
		Size: 440.0 KB (439964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c288a14eff30367048e215968facd583b69208c88f246db36f95de84f9f95f2`  
		Last Modified: Tue, 31 Mar 2020 09:06:04 GMT  
		Size: 230.4 MB (230401952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869ba1a44b39237de723e6eda8cbc9d92fa5702dd1accdffa458c18710105b60`  
		Last Modified: Tue, 31 Mar 2020 09:05:00 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e006598e8f8b8d7108107e4dfe8806ed90da205417bf5afa1a33fc09b12f664a`  
		Last Modified: Tue, 31 Mar 2020 09:06:37 GMT  
		Size: 103.0 MB (102959855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b39fec26b1b23b032c4d2fe4df93c72237b36a58682cc76a7e60d3572c31dd`  
		Last Modified: Tue, 31 Mar 2020 09:08:36 GMT  
		Size: 351.1 MB (351063688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
