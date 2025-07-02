## `ros:humble-perception`

```console
$ docker pull ros@sha256:355eb22220a20608fd81cf6f6ad1425937488082e4a6d6c6d602ed6e178746f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:acf128849a3369507a6a4ceb548b8b88495776e5441fc42fc2f0044a6ff5f341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954901851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3779b408ba04f4d762b59d53198cf1fa73d196c3ce5661a1ffa9cb84d08dbc06`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fd9e74e6fd05a516cea0b71abc9baf18606effe4543e6337901025fbe4eb0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 98.0 MB (97959535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c6f0311484b8b07ef741892d26236263307cdb1798f283cfcca3109fe97a`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 363.5 KB (363513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a88d1d3274993db9497c692378fd53e3a7ef81905672d82b75b5e9b33ffc9`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f8638479e522ab3779b4570a1b2c8d65c44b3d80a4f28e78ac598e1efd1419`  
		Last Modified: Wed, 02 Jul 2025 05:11:20 GMT  
		Size: 23.3 MB (23314712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81167327080034190e8b4afacb869f0b09a72dd3d0ecde42cc9a5c1785c39567`  
		Last Modified: Wed, 02 Jul 2025 08:12:56 GMT  
		Size: 691.9 MB (691870812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ea19cacfab70339d3a693bd9e1f937b81573c5d84e2e5c51b09b11ae2eade7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58716654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec8a2da138eeb95ff9204fd21911a109d9eb9d70f85ff46839f82f342845506`

```dockerfile
```

-	Layers:
	-	`sha256:e786222e804489e19ca314d5ecb462a3df364bea472bcbdd15a6d618606eeb0e`  
		Last Modified: Wed, 02 Jul 2025 07:17:26 GMT  
		Size: 58.7 MB (58707260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce3902ff94e48b704ee061aa1c8ea640ddfd11d15095cb844414418f93be4b5`  
		Last Modified: Wed, 02 Jul 2025 07:17:27 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:72d3d5732dd8247e52175e5a4f54a8cb8c82f192f9dcf96e6eec66fb57ae0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.2 MB (915197125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b7d9255f02d28916a1535996b7cac717bfc6021d8ee29ce80fef94336f63d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfa6906e2ea85de0e1680f6e3c427525e720a8b824f41b6940fba7aefb7fbc`  
		Last Modified: Tue, 03 Jun 2025 17:54:21 GMT  
		Size: 659.8 MB (659788039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:52bc806baf40be74602a3ec21f1ff98a3cdae0f006a8a8cd70ca1cd0a5aa5306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57830168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaf56ee38fa3e8144790a313d51b47c88811c2027edf13eb713f05fd73c25be`

```dockerfile
```

-	Layers:
	-	`sha256:7c7d2a9307f4c8ec88bee684f58d7bd6df5d47b02b7f226c4d4dc21ca5b0c115`  
		Last Modified: Tue, 03 Jun 2025 19:19:18 GMT  
		Size: 57.8 MB (57820693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6d3a2db78d00a8859dd4d555d6cb7c4735c41e9b3e6334ca0e9a105ad0e618`  
		Last Modified: Tue, 03 Jun 2025 19:19:19 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
