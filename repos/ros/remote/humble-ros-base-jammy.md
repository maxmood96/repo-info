## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json
