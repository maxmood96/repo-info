## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:edd733188896f30860e4966f4ba48d68e55d65ffe5e62dab35d0eeaac8c39efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:acc676afebf4c38d34613a768a80e7d9d8eeaa95b630941fef6017a42578ffde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.5 MB (955538683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d23f1ac705fc4ce44aa854383ae0a7e4938c6d8561dce4a2463a93c94621c13`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dec43e28aad1e2cadf4a3049124373963669e4bdc95a2f75e1dd63b3eb7d4`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 98.2 MB (98162262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf5f7cd1537f5913a85f2ebc069c9789e846bf183dff3a228255ff5cec83d5a`  
		Last Modified: Tue, 17 Feb 2026 21:30:23 GMT  
		Size: 385.7 KB (385692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b69186bf79733d3d6b81c46636fc779e193368bc38db8d3010b68876160cf`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561868aa7cf7cf04f054a78bd8ea5432a5e5b7616b392f06e30288df496aa06`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.3 MB (23319467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52268b348904e592ff59e382a161ba93be4dcf836eeafd72c2fa2eaefca6875d`  
		Last Modified: Tue, 17 Feb 2026 21:55:49 GMT  
		Size: 692.1 MB (692123027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e0a3cd1ef3e3f6c71a907a215162c9a85cb84043b07346121859d68ab5fb0c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58802694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105395e78b3d50c31660fd5e1e322b86bc381eefdb239cc3e6ed1989c9ef864a`

```dockerfile
```

-	Layers:
	-	`sha256:01144e078e7cfbc4e9b270382e49fd1f529360038ca5b2eb3613a562e78e90c8`  
		Last Modified: Tue, 17 Feb 2026 21:55:38 GMT  
		Size: 58.8 MB (58793342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71659aa8898127d013ed917a80317dee93c31f9b49503d3a4aba353c74325445`  
		Last Modified: Tue, 17 Feb 2026 21:55:36 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:26e5c42bc916f2c77c59cb38b7c4eb071b92b0a8c65ea6f19691395c299dcdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.0 MB (916045816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741ffae9aa3b34a9e1897ff16652f273bc5798684f8a2d50bb2a45e474ba438d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62216dc13167a74c4b0ea4bceed53adbd12ca59082f9d7d140072fb8303cd3b`  
		Last Modified: Tue, 17 Feb 2026 21:30:43 GMT  
		Size: 95.8 MB (95763594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6985ab4c77e34b80ea8654dbbb36877bb046b39b4e1a89152bff01ec65ae27`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 385.7 KB (385698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2fc45c9db8d6efebbc61a4596bd898b8b84cdbaf4216b4d244de614b5ee3ac`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb3a087f98a0a2ce287e3d474cd5e6ecbbd623963b6f262dd73d5a9f42535c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 22.7 MB (22718722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9099d6f311b19a3abce597dce855a2e4c38498c822ceec77e2e8b8a71fa549`  
		Last Modified: Tue, 17 Feb 2026 21:55:28 GMT  
		Size: 660.1 MB (660066822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:2fa18ac5330e35d1f327a4a0b9565b3774bf97747180760166cd6311213f288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58787095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bab72dea5017b9b3ec1c40fcc1396d3be8271ef37b96e79b33e40cf25006f43`

```dockerfile
```

-	Layers:
	-	`sha256:c036016afe5c3d4f431675ce726bdd329e56f1de8c8efa07bdf97fd2851e2f77`  
		Last Modified: Tue, 17 Feb 2026 21:55:17 GMT  
		Size: 58.8 MB (58777663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30ae5ac2a1bd3937b560515b5a80ce477a27a9b9adbb8a371cee4f2b5783944`  
		Last Modified: Tue, 17 Feb 2026 21:55:14 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
