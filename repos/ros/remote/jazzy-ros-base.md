## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:e3975c54bbb607329a5fd03297aa2c2c82ee90e2406a4bbebfdacc4228d5a555
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:7f115cc6266a06edac7e619293ce1a9abc747c8e3dec91dddfee7d68ffadabcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295897654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a3b0409bcba5cc95830549d58fc7b6d00f582351301d2211e2de7274c47554`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad268d3577575b8a090cd6e684e1bfe2743e4ff225fd68d59f6cc8d1311efc1`  
		Last Modified: Tue, 02 Sep 2025 00:13:52 GMT  
		Size: 683.8 KB (683827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8905021a0e9d1029ab7dd7f84415090e39e65ca21a7df47ef3c9979f86d6f8a`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 6.7 MB (6746681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b374353b323cb503e72f9217993e9545747c2635f474858cf301ab4eb3dc7e2`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 94.1 KB (94067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948960a889906032c1cfe6c7576e66036370fc2303edc1886125832bb4feb838`  
		Last Modified: Tue, 02 Sep 2025 00:23:50 GMT  
		Size: 120.1 MB (120091608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2cb1a3fd6fea1facb4eefd901cc55e8b4e196e5ece372ee5fbe3602870e7c`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610e404c741cc3157322e2ddcca15d30da2fb7f346eb3465a091b20317ca5878`  
		Last Modified: Tue, 02 Sep 2025 01:12:32 GMT  
		Size: 110.2 MB (110182606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779737f31af27db752ae2b99cf2d51c8c6c371e8ccb1df300402aac7393fd530`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 375.5 KB (375470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c14724f62e3a3f80af2cc44890e7744dbdfac3a41424fa477b97263802bf909`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bf222367561b42fb0e9b4a01be0b7f986ed37fd538e5bb7df4223ffe7d8d22`  
		Last Modified: Tue, 02 Sep 2025 01:12:28 GMT  
		Size: 28.0 MB (27997635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b656819aa97d6a1d8810e8c976997391ae2f9f0bb44bd3a2059dd5d477c1634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6320738f023d5c7d07d28e7a0513c9b2f3051e213d755813ffe3b99b2f043caa`

```dockerfile
```

-	Layers:
	-	`sha256:f32b874de7a2e8c44b4a586290104742135a13db017fcef4ecea204b58f97d94`  
		Last Modified: Tue, 02 Sep 2025 04:17:37 GMT  
		Size: 24.5 MB (24543450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da361f88e5269782ba53e32a6bb5556aedb6448fa8c75da47700407ed704ef05`  
		Last Modified: Tue, 02 Sep 2025 04:17:38 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:084f8be27c2a80f8393f8b6c543ab55c774c76c143e5fe4cf2c600bca1df91a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284163609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15139885c35a357478d1a302a215326902773be30947a0493df3a22a749449e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4fca2469212f7c463fa14e87fe769d2a219fecf58125d538219a566e9b9ec9`  
		Last Modified: Tue, 12 Aug 2025 21:07:03 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8101d7e467e40dcfb7a696c7d00d28a9434914ea87bae800f81106c8e471f29e`  
		Last Modified: Tue, 12 Aug 2025 21:07:03 GMT  
		Size: 6.8 MB (6759892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883862c530c4be898d18cd02b3b2123fa8a5ea159a5132eca0eef18580a0faa5`  
		Last Modified: Tue, 12 Aug 2025 21:07:02 GMT  
		Size: 94.2 KB (94211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaf5d61dd644cf3d3fa7d5d4502c9489f9b1d9aac086a9a2e589df10b2fa8f3`  
		Last Modified: Tue, 12 Aug 2025 21:07:13 GMT  
		Size: 114.7 MB (114725153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fb69aeb6c25e0d3359d612bf82eb10e922983c26f7d8197a2880133f9a6040`  
		Last Modified: Tue, 12 Aug 2025 21:07:04 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bad8dca98e020d82514831a5ae73bc7a25099ece8ba9e4b33285f7e49a80da9`  
		Last Modified: Wed, 13 Aug 2025 02:16:21 GMT  
		Size: 105.6 MB (105590785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2bc9318d7ff64f1d0e245ef7e3fd8f2771e0dfb8d466c76b36a771f82ed441`  
		Last Modified: Wed, 13 Aug 2025 00:18:37 GMT  
		Size: 373.9 KB (373948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9bf2085174a0adddd8103d0495a2b347afc6ba934cf8a1944e28324535d696`  
		Last Modified: Wed, 13 Aug 2025 00:18:40 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c9974406eb620a2ef77189c60c0eea209418e05e59f0786525b3fead1eef67`  
		Last Modified: Wed, 13 Aug 2025 02:16:13 GMT  
		Size: 27.1 MB (27072626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6d95355a97f163666fd2f5c671c43e4013164fc7fafac2ab024952923e7dee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24568694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2f8ffcf63f003ba99f814960f358f64e3743b08d7a004ee6f1ea3783561e3a`

```dockerfile
```

-	Layers:
	-	`sha256:c069e1f97861b84332cf47ac0397addf84d5a311f16cebf83b43aca66e275ec8`  
		Last Modified: Wed, 13 Aug 2025 01:17:49 GMT  
		Size: 24.6 MB (24551882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700fee9327931b8577bfce92759b813afb6cede3b5a1ca2c294bb1879b6e90fe`  
		Last Modified: Wed, 13 Aug 2025 01:17:50 GMT  
		Size: 16.8 KB (16812 bytes)  
		MIME: application/vnd.in-toto+json
