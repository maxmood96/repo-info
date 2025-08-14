## `ros:jazzy`

```console
$ docker pull ros@sha256:69777db2f4e08c94b309e5348a95ab14eb4bb2cff034f3b65f98b648877807f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:d95566492463c55583c3749da702298a68059d44d64f2f4a8b1615cd2e2f1cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295720754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942e3c271725913d241572f8e721fcc8aaf985dcb85c62c6656e679003c02eba`
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
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5669da1476ae49de63191f7ab508916de120191944714d3f59fd168bc962bfa8`  
		Last Modified: Tue, 12 Aug 2025 17:56:17 GMT  
		Size: 683.8 KB (683835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779376049a708f862811da0326662e38e6ffaf7f671f181619ca7995dc1dfd00`  
		Last Modified: Tue, 12 Aug 2025 17:56:18 GMT  
		Size: 6.7 MB (6746801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a05b6de8956d3104f334cd64b6be0e1b4d1535625cfac4bf1719efec90e99`  
		Last Modified: Tue, 12 Aug 2025 17:56:17 GMT  
		Size: 94.1 KB (94071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692b7c24f1a53d4ef41b9fde907dbefdb629d4a1bedadca90dc47611c071aa18`  
		Last Modified: Tue, 12 Aug 2025 17:56:26 GMT  
		Size: 119.9 MB (119948109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5729cba7f178584b3f04587d7d1782810c05f07b22048ed72717d3cc5f5c079`  
		Last Modified: Tue, 12 Aug 2025 17:56:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16843ee9700cba3c9a936c59435844b2839668d9dc3b89e31d62e88f41abe12`  
		Last Modified: Tue, 12 Aug 2025 17:58:28 GMT  
		Size: 110.2 MB (110182062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a615cd94c2eabfae80030b452ef43e01ec067a7e0be8637d4e2f8592f69c65a`  
		Last Modified: Tue, 12 Aug 2025 17:58:12 GMT  
		Size: 374.0 KB (373952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cf47cf97ded230828253a36f0a2072feb9b7a175e3bd4d4dfa0c0272e4c625`  
		Last Modified: Tue, 12 Aug 2025 17:58:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc0b8d06e27278def2dbf7151f73990785ceac0f06041e81480665d933da601`  
		Last Modified: Tue, 12 Aug 2025 17:58:11 GMT  
		Size: 28.0 MB (27966019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:0029e25e031d215f3afb4be8ee2bd488d17a18d44f949911bf39a2f0437033eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24546273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8536558397b090e0dfbdf9f5ba6a6ee63c415f8fc7ef8359381d7e5519e1bc1e`

```dockerfile
```

-	Layers:
	-	`sha256:e2f4a3fa9f1aea9a02c9a5d54c6348535ce3be1266e951f03d7102b78b7ee8fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:43 GMT  
		Size: 24.5 MB (24529609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3e579bd6f2bd3290a2b2dc61a7d57bbc7c1b41e5022bf679a625775397bc1e7`  
		Last Modified: Tue, 12 Aug 2025 19:17:44 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

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

### `ros:jazzy` - unknown; unknown

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
