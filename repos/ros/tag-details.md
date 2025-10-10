<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:kilted`](#roskilted)
-	[`ros:kilted-perception`](#roskilted-perception)
-	[`ros:kilted-perception-noble`](#roskilted-perception-noble)
-	[`ros:kilted-ros-base`](#roskilted-ros-base)
-	[`ros:kilted-ros-base-noble`](#roskilted-ros-base-noble)
-	[`ros:kilted-ros-core`](#roskilted-ros-core)
-	[`ros:kilted-ros-core-noble`](#roskilted-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:dfc94c85d8e01f230951b2a85ca5576e08473081c3da5fbbe8f3ab844703b9ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:65e1667d4e6c30a38de60decfcda2b3617bf8e5d3e34e809ff02fde9ca98809f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263100341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a99e0ca6f90d65ebd0edc4158bd00dadbda34b8beabb0e6d3b63171b8ea7d30`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:c32a70701dc37f4de5e5fe2b02d4475d1df89b1611daef77ae8857612a640985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23692609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e7e0eabf24e41f8636df72f6d253d696fffb7fa889da7b89e7527d920f0597`

```dockerfile
```

-	Layers:
	-	`sha256:ccff4c15f493db928845a89510cd01b5a431e9ba46b8d82d69010f7f62aedb5c`  
		Last Modified: Thu, 02 Oct 2025 10:17:18 GMT  
		Size: 23.7 MB (23676218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1a4be4bf243137b72ede78af4b3007d6c0ddba7bfec77c894e85d0027e96bf`  
		Last Modified: Thu, 02 Oct 2025 10:17:20 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:584d92e06114bb0345ccd7c725675450bfce6858e2f84059d6f35cca600bbc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255605104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3838025806507338eaa1c756e29eddf105710a30f50322d3e9748049fbff3e`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:6d81510c4e685db25305929a560e9f1314cce4fb4b0c8f74ce7d3057cab9b6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23705763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a07a9953aeff232be0b5d25a51cda0a47207378e64ad0c20228d97793380c7`

```dockerfile
```

-	Layers:
	-	`sha256:8faa529f7422b290979a8f1b5164cd423a55030e133010735fa5dabd97362c7e`  
		Last Modified: Thu, 02 Oct 2025 04:17:39 GMT  
		Size: 23.7 MB (23689235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c266441efaba0e4768ff012666ab836bd71be4c52ec21d1282885b7d0e10a5`  
		Last Modified: Thu, 02 Oct 2025 04:17:40 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:b28e43e044e231ed2f13f6d351586191037e6ff4de8dfd49c8bba7c4ef59575b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:cd95809fb5038fd44edf79e271b48038a9f54c803dd057cfab4ada139d4da977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.2 MB (955165950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38c757f5c9847defc2c884ec0dea713341a46d4c57f4085f9af2de9f437edd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec12be7f73945dd776113708f0deb24b26153cebc4a2cfbfb92753be821195`  
		Last Modified: Thu, 02 Oct 2025 13:18:33 GMT  
		Size: 692.1 MB (692065609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3abbef0fd6d5fd5a1af78a6568be69ccde5283c27d7e6c56b0c8ca00d1f66c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58777209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b97d9adebcc2f4b35c1c7f94788fd4d2191fca9d9801f63466c41828f8ed11`

```dockerfile
```

-	Layers:
	-	`sha256:c4dc946f3e88502c233637ff403efcca49da9f493ba42cb19ea6ec5c40d70b3a`  
		Last Modified: Thu, 02 Oct 2025 13:17:21 GMT  
		Size: 58.8 MB (58767814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad2bd5128e7058c90801145de9f9fa359dfe880c2a2290bb8ca0a4b1f1fd1d1`  
		Last Modified: Thu, 02 Oct 2025 13:17:22 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3b3b6ff97b4b53dd43e628fafbb647a88f6f51221d42d95c2bdf2223357f6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915609144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0d501c7ddfa99ac60b138d72d94f81ea235108131d6732a35a4f3f8011ab2`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e2cb20c1dc183518b13ed55eccd22d11d50b212a21d414606337cc6c9dfa8`  
		Last Modified: Thu, 02 Oct 2025 04:21:25 GMT  
		Size: 660.0 MB (660004040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:95b26e59188683835237e4192a1143316b84eaff8fe03e7b9c33c92e1101a8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58761610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd567ee08a59ee70095b9e58ed96d33edd2ddf1154a0ca31f825d9da5e75bd3`

```dockerfile
```

-	Layers:
	-	`sha256:919c156d38ce0596b3d6b68493b917d2213f9ac75124f2e6c45cf24ab74b5e9f`  
		Last Modified: Thu, 02 Oct 2025 04:19:12 GMT  
		Size: 58.8 MB (58752135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a37e5fdd450e9e532057f7bb383c800c970154102b4dabb6d8170b92d8bbb5`  
		Last Modified: Thu, 02 Oct 2025 04:19:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:b28e43e044e231ed2f13f6d351586191037e6ff4de8dfd49c8bba7c4ef59575b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:cd95809fb5038fd44edf79e271b48038a9f54c803dd057cfab4ada139d4da977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.2 MB (955165950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38c757f5c9847defc2c884ec0dea713341a46d4c57f4085f9af2de9f437edd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec12be7f73945dd776113708f0deb24b26153cebc4a2cfbfb92753be821195`  
		Last Modified: Thu, 02 Oct 2025 13:18:33 GMT  
		Size: 692.1 MB (692065609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3abbef0fd6d5fd5a1af78a6568be69ccde5283c27d7e6c56b0c8ca00d1f66c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58777209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b97d9adebcc2f4b35c1c7f94788fd4d2191fca9d9801f63466c41828f8ed11`

```dockerfile
```

-	Layers:
	-	`sha256:c4dc946f3e88502c233637ff403efcca49da9f493ba42cb19ea6ec5c40d70b3a`  
		Last Modified: Thu, 02 Oct 2025 13:17:21 GMT  
		Size: 58.8 MB (58767814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad2bd5128e7058c90801145de9f9fa359dfe880c2a2290bb8ca0a4b1f1fd1d1`  
		Last Modified: Thu, 02 Oct 2025 13:17:22 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3b3b6ff97b4b53dd43e628fafbb647a88f6f51221d42d95c2bdf2223357f6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915609144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0d501c7ddfa99ac60b138d72d94f81ea235108131d6732a35a4f3f8011ab2`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e2cb20c1dc183518b13ed55eccd22d11d50b212a21d414606337cc6c9dfa8`  
		Last Modified: Thu, 02 Oct 2025 04:21:25 GMT  
		Size: 660.0 MB (660004040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:95b26e59188683835237e4192a1143316b84eaff8fe03e7b9c33c92e1101a8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58761610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd567ee08a59ee70095b9e58ed96d33edd2ddf1154a0ca31f825d9da5e75bd3`

```dockerfile
```

-	Layers:
	-	`sha256:919c156d38ce0596b3d6b68493b917d2213f9ac75124f2e6c45cf24ab74b5e9f`  
		Last Modified: Thu, 02 Oct 2025 04:19:12 GMT  
		Size: 58.8 MB (58752135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a37e5fdd450e9e532057f7bb383c800c970154102b4dabb6d8170b92d8bbb5`  
		Last Modified: Thu, 02 Oct 2025 04:19:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:dfc94c85d8e01f230951b2a85ca5576e08473081c3da5fbbe8f3ab844703b9ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:65e1667d4e6c30a38de60decfcda2b3617bf8e5d3e34e809ff02fde9ca98809f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263100341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a99e0ca6f90d65ebd0edc4158bd00dadbda34b8beabb0e6d3b63171b8ea7d30`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:c32a70701dc37f4de5e5fe2b02d4475d1df89b1611daef77ae8857612a640985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23692609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e7e0eabf24e41f8636df72f6d253d696fffb7fa889da7b89e7527d920f0597`

```dockerfile
```

-	Layers:
	-	`sha256:ccff4c15f493db928845a89510cd01b5a431e9ba46b8d82d69010f7f62aedb5c`  
		Last Modified: Thu, 02 Oct 2025 10:17:18 GMT  
		Size: 23.7 MB (23676218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1a4be4bf243137b72ede78af4b3007d6c0ddba7bfec77c894e85d0027e96bf`  
		Last Modified: Thu, 02 Oct 2025 10:17:20 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:584d92e06114bb0345ccd7c725675450bfce6858e2f84059d6f35cca600bbc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255605104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3838025806507338eaa1c756e29eddf105710a30f50322d3e9748049fbff3e`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6d81510c4e685db25305929a560e9f1314cce4fb4b0c8f74ce7d3057cab9b6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23705763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a07a9953aeff232be0b5d25a51cda0a47207378e64ad0c20228d97793380c7`

```dockerfile
```

-	Layers:
	-	`sha256:8faa529f7422b290979a8f1b5164cd423a55030e133010735fa5dabd97362c7e`  
		Last Modified: Thu, 02 Oct 2025 04:17:39 GMT  
		Size: 23.7 MB (23689235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c266441efaba0e4768ff012666ab836bd71be4c52ec21d1282885b7d0e10a5`  
		Last Modified: Thu, 02 Oct 2025 04:17:40 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:dfc94c85d8e01f230951b2a85ca5576e08473081c3da5fbbe8f3ab844703b9ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:65e1667d4e6c30a38de60decfcda2b3617bf8e5d3e34e809ff02fde9ca98809f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263100341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a99e0ca6f90d65ebd0edc4158bd00dadbda34b8beabb0e6d3b63171b8ea7d30`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:c32a70701dc37f4de5e5fe2b02d4475d1df89b1611daef77ae8857612a640985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23692609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e7e0eabf24e41f8636df72f6d253d696fffb7fa889da7b89e7527d920f0597`

```dockerfile
```

-	Layers:
	-	`sha256:ccff4c15f493db928845a89510cd01b5a431e9ba46b8d82d69010f7f62aedb5c`  
		Last Modified: Thu, 02 Oct 2025 10:17:18 GMT  
		Size: 23.7 MB (23676218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1a4be4bf243137b72ede78af4b3007d6c0ddba7bfec77c894e85d0027e96bf`  
		Last Modified: Thu, 02 Oct 2025 10:17:20 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:584d92e06114bb0345ccd7c725675450bfce6858e2f84059d6f35cca600bbc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255605104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3838025806507338eaa1c756e29eddf105710a30f50322d3e9748049fbff3e`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:6d81510c4e685db25305929a560e9f1314cce4fb4b0c8f74ce7d3057cab9b6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23705763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a07a9953aeff232be0b5d25a51cda0a47207378e64ad0c20228d97793380c7`

```dockerfile
```

-	Layers:
	-	`sha256:8faa529f7422b290979a8f1b5164cd423a55030e133010735fa5dabd97362c7e`  
		Last Modified: Thu, 02 Oct 2025 04:17:39 GMT  
		Size: 23.7 MB (23689235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c266441efaba0e4768ff012666ab836bd71be4c52ec21d1282885b7d0e10a5`  
		Last Modified: Thu, 02 Oct 2025 04:17:40 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:6ed1fd72ca4c2fef457137a2cdc39c428eb7862a73e81c4d1e8ac716744967b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e46ca5e7bf441e70600df3d67e4107e2b80466d18f453aab69920b6d32d605a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141443960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c45d7c9de5b335742cb4b89a175345cd34fd455ddb170a58003df8c2964cb5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:42baf941e6eb748a37eadcdadc58b691d84c3bd98cc000eff00a7fffb83eef97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17670671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d8430d5d98c928a7b8251855fcfe170b1e9aade0a02ef79d7ac7994bdcca68`

```dockerfile
```

-	Layers:
	-	`sha256:bc1fe717297701c804bf12d76086cd72b4d0e93c25c4da67db0f54d10b10d216`  
		Last Modified: Thu, 02 Oct 2025 07:17:22 GMT  
		Size: 17.7 MB (17656014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b70e26d40bae7a44f42fd191ff8d4adb14fca219468dedf0495db5ad1441de`  
		Last Modified: Thu, 02 Oct 2025 07:17:23 GMT  
		Size: 14.7 KB (14657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0899ad26ccd9c74796e211ea2644bbee71f3a2c4d6e75ba51766d260b1ee8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136976213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b9f429610957b1ed0281582613c9b9cc9995f7a5744a03900378a8c246ff87`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:2bf640241e4bd9623fb66b42001d73ae1b4a368e884f6e56e8e49fcda789a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17657141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad3b4c5676b77a35c156acf6bcb137cff3587b86a515d59974fed0fdf987d67`

```dockerfile
```

-	Layers:
	-	`sha256:3f5970fc58fb353a2be489a88540cfdd799a23d1302517aad0133eb6c08bd4ab`  
		Last Modified: Thu, 02 Oct 2025 04:17:53 GMT  
		Size: 17.6 MB (17642359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d89ec309597255858a459e105acce87c5720036421d990e32b355eb137e855`  
		Last Modified: Thu, 02 Oct 2025 04:17:54 GMT  
		Size: 14.8 KB (14782 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:6ed1fd72ca4c2fef457137a2cdc39c428eb7862a73e81c4d1e8ac716744967b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e46ca5e7bf441e70600df3d67e4107e2b80466d18f453aab69920b6d32d605a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141443960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c45d7c9de5b335742cb4b89a175345cd34fd455ddb170a58003df8c2964cb5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:42baf941e6eb748a37eadcdadc58b691d84c3bd98cc000eff00a7fffb83eef97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17670671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d8430d5d98c928a7b8251855fcfe170b1e9aade0a02ef79d7ac7994bdcca68`

```dockerfile
```

-	Layers:
	-	`sha256:bc1fe717297701c804bf12d76086cd72b4d0e93c25c4da67db0f54d10b10d216`  
		Last Modified: Thu, 02 Oct 2025 07:17:22 GMT  
		Size: 17.7 MB (17656014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b70e26d40bae7a44f42fd191ff8d4adb14fca219468dedf0495db5ad1441de`  
		Last Modified: Thu, 02 Oct 2025 07:17:23 GMT  
		Size: 14.7 KB (14657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0899ad26ccd9c74796e211ea2644bbee71f3a2c4d6e75ba51766d260b1ee8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136976213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b9f429610957b1ed0281582613c9b9cc9995f7a5744a03900378a8c246ff87`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:2bf640241e4bd9623fb66b42001d73ae1b4a368e884f6e56e8e49fcda789a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17657141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad3b4c5676b77a35c156acf6bcb137cff3587b86a515d59974fed0fdf987d67`

```dockerfile
```

-	Layers:
	-	`sha256:3f5970fc58fb353a2be489a88540cfdd799a23d1302517aad0133eb6c08bd4ab`  
		Last Modified: Thu, 02 Oct 2025 04:17:53 GMT  
		Size: 17.6 MB (17642359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d89ec309597255858a459e105acce87c5720036421d990e32b355eb137e855`  
		Last Modified: Thu, 02 Oct 2025 04:17:54 GMT  
		Size: 14.8 KB (14782 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:6616419d6752d8ef5822f774332a6d845ef909b9f28454428b4dadacf83f4d6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:21ca684a69663bce262ef38b418ceff778dc8d056d69fc9cdfe3b165a4f79baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298320939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94767efcadc98a9f3ba867d6e5393774aa6b16b0acdc42c7fc8fa71b096a9125`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8bb927407dff4c86a177c9405741da663a12e7437133c81c62c81e2449e128`  
		Last Modified: Thu, 02 Oct 2025 05:18:07 GMT  
		Size: 683.9 KB (683867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd9f21b79e9e7e0ad635ba1a0a6b43c12e475289642f226f9e319bd5ea695d`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 9.1 MB (9147634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611dec3b085de3fbf3f81cbb44b6455eb23dc88e6dc09b64612a281b23cc9503`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 94.2 KB (94194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860cf45bc9590dfdc2f85a44991d355a3ea1a413aee3c6e1d492d14f4c3aa61`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 120.1 MB (120110330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966aa943b4b80bfd43fd9d346c621bb5e892b996fbafb736be801a8cffb8c533`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ed68fe206c42cfc647439c7dc83490be9f02d80f59772c0dbdf465c0f`  
		Last Modified: Thu, 02 Oct 2025 08:43:08 GMT  
		Size: 110.2 MB (110182298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c7f1f3966277d41eed6bc49ebec744e08dad8b9fee5c18c228ca040a514c`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56e56c16231d651035aa39e28cdadcd9a7944f8fd4121a0ce2e4d572c74345`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652e2dc1413588e623e18b712880047f39297cc468a08211cafdb8e384ed807`  
		Last Modified: Thu, 02 Oct 2025 08:43:05 GMT  
		Size: 28.0 MB (27998640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:6ab5b327b6bd6047607329f6741b3a38ecfaf409b4be319fe41d3bb611167e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f2048fc8bd5a8f2e9d68ea9921978ee8a2363108eb9ebb81683e652b3e7e5b`

```dockerfile
```

-	Layers:
	-	`sha256:73e777a6ccf4e32505263cf2bf6511bd5fb3e67a28d20ade0fc1f0a604c8b089`  
		Last Modified: Thu, 02 Oct 2025 10:17:36 GMT  
		Size: 24.5 MB (24543454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc5faa4f50770c1503c4f2512ad8317ee2e0a249f136176757377dc1d82c04`  
		Last Modified: Thu, 02 Oct 2025 10:17:37 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d0e5b652b7bc395b79e6bff9e10e35e862a5adfc7ebd756d0a198faa2c0eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286576562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b913ca6da461594facd10ff82b6ea5e40e574b18ceec831c3b7ad5673dc06f52`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:c2f7c6c797eea4625f53276251170cff19433ffb3f5e9e3c53284d3f2efb08c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24582540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff22f022cce7b94679cd1f691bf2f478261c95ef41fc1f7b39d4905082e987e`

```dockerfile
```

-	Layers:
	-	`sha256:36155c38a5edb438516abb1f20660b99bbc32576ac6b765d7e5c63706c578e5c`  
		Last Modified: Thu, 02 Oct 2025 04:18:05 GMT  
		Size: 24.6 MB (24565727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f26318a42f5ecbcc048c1478bffee73eb09c82fdf00ce4c1242b859c846482`  
		Last Modified: Thu, 02 Oct 2025 04:18:06 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:4e00a5a01fd6fbfc44898b16f8ff78e4b49678160208a26b35872586eb631485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:bb339b55b4d744445522485f8b30c1b8b0c105882c685540003c550d89d3e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082789626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bd58e41485b36829ce6b90d7ec2d4413e945c0947a326ecf4a38b96629c01e`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8bb927407dff4c86a177c9405741da663a12e7437133c81c62c81e2449e128`  
		Last Modified: Thu, 02 Oct 2025 05:18:07 GMT  
		Size: 683.9 KB (683867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd9f21b79e9e7e0ad635ba1a0a6b43c12e475289642f226f9e319bd5ea695d`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 9.1 MB (9147634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611dec3b085de3fbf3f81cbb44b6455eb23dc88e6dc09b64612a281b23cc9503`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 94.2 KB (94194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860cf45bc9590dfdc2f85a44991d355a3ea1a413aee3c6e1d492d14f4c3aa61`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 120.1 MB (120110330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966aa943b4b80bfd43fd9d346c621bb5e892b996fbafb736be801a8cffb8c533`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ed68fe206c42cfc647439c7dc83490be9f02d80f59772c0dbdf465c0f`  
		Last Modified: Thu, 02 Oct 2025 08:43:08 GMT  
		Size: 110.2 MB (110182298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c7f1f3966277d41eed6bc49ebec744e08dad8b9fee5c18c228ca040a514c`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56e56c16231d651035aa39e28cdadcd9a7944f8fd4121a0ce2e4d572c74345`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652e2dc1413588e623e18b712880047f39297cc468a08211cafdb8e384ed807`  
		Last Modified: Thu, 02 Oct 2025 08:43:05 GMT  
		Size: 28.0 MB (27998640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe337f4845a74fd5af6f7ff0d6b6911d13909265155a660d1a7c75136e7d24d6`  
		Last Modified: Thu, 02 Oct 2025 13:46:29 GMT  
		Size: 784.5 MB (784468687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e024495a4c6b69c17c1a4e648a9df8478fad38b13d2ebc18c9ad44d84da8d8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7ada73dcec424c7f501addf4bf78338763db75faa516a2298482dbef239793`

```dockerfile
```

-	Layers:
	-	`sha256:4737d46ca4954eb44f5866f827ff80f8e320d3696b1fed402ad9436f0acfcf89`  
		Last Modified: Thu, 02 Oct 2025 13:17:32 GMT  
		Size: 60.7 MB (60705333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769ccfa227e9b8a89d52ecc50be7822336142e99eea9239d745f534c2d2f1c14`  
		Last Modified: Thu, 02 Oct 2025 13:17:34 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:82a6d42cb15422a5f2c616a3e73260ff7c9ccf74ddea7d78bf4b43620938f4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.1 MB (981053173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a40b9c5cb1e07160696b9e2e953f049ded0f3d2601b4f777c2cec57705b05`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe901845c92843e795d45ed02555a34ddf850cd17fa3277fad5ccc4f6335cf05`  
		Last Modified: Thu, 02 Oct 2025 04:20:58 GMT  
		Size: 694.5 MB (694476611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9b317f917be5833fa35c539d949e91772417e479938718845ecd825c4144c063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37daa022ed20683574190e33878160caa05109cc607086f6cb47b07e54ece4b5`

```dockerfile
```

-	Layers:
	-	`sha256:4a169c9a00bf7b15820b30af17e66748ba1222e7745992f7e8303d51e1e6e112`  
		Last Modified: Thu, 02 Oct 2025 04:19:14 GMT  
		Size: 60.6 MB (60635858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3bf512451230e1aaae8975379457dea5fa2dd4c7dde060a9ae682fa89d5208`  
		Last Modified: Thu, 02 Oct 2025 04:19:15 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:4e00a5a01fd6fbfc44898b16f8ff78e4b49678160208a26b35872586eb631485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:bb339b55b4d744445522485f8b30c1b8b0c105882c685540003c550d89d3e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082789626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bd58e41485b36829ce6b90d7ec2d4413e945c0947a326ecf4a38b96629c01e`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8bb927407dff4c86a177c9405741da663a12e7437133c81c62c81e2449e128`  
		Last Modified: Thu, 02 Oct 2025 05:18:07 GMT  
		Size: 683.9 KB (683867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd9f21b79e9e7e0ad635ba1a0a6b43c12e475289642f226f9e319bd5ea695d`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 9.1 MB (9147634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611dec3b085de3fbf3f81cbb44b6455eb23dc88e6dc09b64612a281b23cc9503`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 94.2 KB (94194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860cf45bc9590dfdc2f85a44991d355a3ea1a413aee3c6e1d492d14f4c3aa61`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 120.1 MB (120110330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966aa943b4b80bfd43fd9d346c621bb5e892b996fbafb736be801a8cffb8c533`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ed68fe206c42cfc647439c7dc83490be9f02d80f59772c0dbdf465c0f`  
		Last Modified: Thu, 02 Oct 2025 08:43:08 GMT  
		Size: 110.2 MB (110182298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c7f1f3966277d41eed6bc49ebec744e08dad8b9fee5c18c228ca040a514c`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56e56c16231d651035aa39e28cdadcd9a7944f8fd4121a0ce2e4d572c74345`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652e2dc1413588e623e18b712880047f39297cc468a08211cafdb8e384ed807`  
		Last Modified: Thu, 02 Oct 2025 08:43:05 GMT  
		Size: 28.0 MB (27998640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe337f4845a74fd5af6f7ff0d6b6911d13909265155a660d1a7c75136e7d24d6`  
		Last Modified: Thu, 02 Oct 2025 13:46:29 GMT  
		Size: 784.5 MB (784468687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e024495a4c6b69c17c1a4e648a9df8478fad38b13d2ebc18c9ad44d84da8d8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7ada73dcec424c7f501addf4bf78338763db75faa516a2298482dbef239793`

```dockerfile
```

-	Layers:
	-	`sha256:4737d46ca4954eb44f5866f827ff80f8e320d3696b1fed402ad9436f0acfcf89`  
		Last Modified: Thu, 02 Oct 2025 13:17:32 GMT  
		Size: 60.7 MB (60705333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769ccfa227e9b8a89d52ecc50be7822336142e99eea9239d745f534c2d2f1c14`  
		Last Modified: Thu, 02 Oct 2025 13:17:34 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:82a6d42cb15422a5f2c616a3e73260ff7c9ccf74ddea7d78bf4b43620938f4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.1 MB (981053173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a40b9c5cb1e07160696b9e2e953f049ded0f3d2601b4f777c2cec57705b05`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe901845c92843e795d45ed02555a34ddf850cd17fa3277fad5ccc4f6335cf05`  
		Last Modified: Thu, 02 Oct 2025 04:20:58 GMT  
		Size: 694.5 MB (694476611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9b317f917be5833fa35c539d949e91772417e479938718845ecd825c4144c063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37daa022ed20683574190e33878160caa05109cc607086f6cb47b07e54ece4b5`

```dockerfile
```

-	Layers:
	-	`sha256:4a169c9a00bf7b15820b30af17e66748ba1222e7745992f7e8303d51e1e6e112`  
		Last Modified: Thu, 02 Oct 2025 04:19:14 GMT  
		Size: 60.6 MB (60635858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3bf512451230e1aaae8975379457dea5fa2dd4c7dde060a9ae682fa89d5208`  
		Last Modified: Thu, 02 Oct 2025 04:19:15 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:6616419d6752d8ef5822f774332a6d845ef909b9f28454428b4dadacf83f4d6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:21ca684a69663bce262ef38b418ceff778dc8d056d69fc9cdfe3b165a4f79baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298320939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94767efcadc98a9f3ba867d6e5393774aa6b16b0acdc42c7fc8fa71b096a9125`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8bb927407dff4c86a177c9405741da663a12e7437133c81c62c81e2449e128`  
		Last Modified: Thu, 02 Oct 2025 05:18:07 GMT  
		Size: 683.9 KB (683867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd9f21b79e9e7e0ad635ba1a0a6b43c12e475289642f226f9e319bd5ea695d`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 9.1 MB (9147634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611dec3b085de3fbf3f81cbb44b6455eb23dc88e6dc09b64612a281b23cc9503`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 94.2 KB (94194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860cf45bc9590dfdc2f85a44991d355a3ea1a413aee3c6e1d492d14f4c3aa61`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 120.1 MB (120110330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966aa943b4b80bfd43fd9d346c621bb5e892b996fbafb736be801a8cffb8c533`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ed68fe206c42cfc647439c7dc83490be9f02d80f59772c0dbdf465c0f`  
		Last Modified: Thu, 02 Oct 2025 08:43:08 GMT  
		Size: 110.2 MB (110182298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c7f1f3966277d41eed6bc49ebec744e08dad8b9fee5c18c228ca040a514c`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56e56c16231d651035aa39e28cdadcd9a7944f8fd4121a0ce2e4d572c74345`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652e2dc1413588e623e18b712880047f39297cc468a08211cafdb8e384ed807`  
		Last Modified: Thu, 02 Oct 2025 08:43:05 GMT  
		Size: 28.0 MB (27998640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6ab5b327b6bd6047607329f6741b3a38ecfaf409b4be319fe41d3bb611167e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f2048fc8bd5a8f2e9d68ea9921978ee8a2363108eb9ebb81683e652b3e7e5b`

```dockerfile
```

-	Layers:
	-	`sha256:73e777a6ccf4e32505263cf2bf6511bd5fb3e67a28d20ade0fc1f0a604c8b089`  
		Last Modified: Thu, 02 Oct 2025 10:17:36 GMT  
		Size: 24.5 MB (24543454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc5faa4f50770c1503c4f2512ad8317ee2e0a249f136176757377dc1d82c04`  
		Last Modified: Thu, 02 Oct 2025 10:17:37 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d0e5b652b7bc395b79e6bff9e10e35e862a5adfc7ebd756d0a198faa2c0eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286576562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b913ca6da461594facd10ff82b6ea5e40e574b18ceec831c3b7ad5673dc06f52`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:c2f7c6c797eea4625f53276251170cff19433ffb3f5e9e3c53284d3f2efb08c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24582540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff22f022cce7b94679cd1f691bf2f478261c95ef41fc1f7b39d4905082e987e`

```dockerfile
```

-	Layers:
	-	`sha256:36155c38a5edb438516abb1f20660b99bbc32576ac6b765d7e5c63706c578e5c`  
		Last Modified: Thu, 02 Oct 2025 04:18:05 GMT  
		Size: 24.6 MB (24565727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f26318a42f5ecbcc048c1478bffee73eb09c82fdf00ce4c1242b859c846482`  
		Last Modified: Thu, 02 Oct 2025 04:18:06 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:6616419d6752d8ef5822f774332a6d845ef909b9f28454428b4dadacf83f4d6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:21ca684a69663bce262ef38b418ceff778dc8d056d69fc9cdfe3b165a4f79baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298320939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94767efcadc98a9f3ba867d6e5393774aa6b16b0acdc42c7fc8fa71b096a9125`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8bb927407dff4c86a177c9405741da663a12e7437133c81c62c81e2449e128`  
		Last Modified: Thu, 02 Oct 2025 05:18:07 GMT  
		Size: 683.9 KB (683867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd9f21b79e9e7e0ad635ba1a0a6b43c12e475289642f226f9e319bd5ea695d`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 9.1 MB (9147634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611dec3b085de3fbf3f81cbb44b6455eb23dc88e6dc09b64612a281b23cc9503`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 94.2 KB (94194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860cf45bc9590dfdc2f85a44991d355a3ea1a413aee3c6e1d492d14f4c3aa61`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 120.1 MB (120110330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966aa943b4b80bfd43fd9d346c621bb5e892b996fbafb736be801a8cffb8c533`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ed68fe206c42cfc647439c7dc83490be9f02d80f59772c0dbdf465c0f`  
		Last Modified: Thu, 02 Oct 2025 08:43:08 GMT  
		Size: 110.2 MB (110182298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c7f1f3966277d41eed6bc49ebec744e08dad8b9fee5c18c228ca040a514c`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56e56c16231d651035aa39e28cdadcd9a7944f8fd4121a0ce2e4d572c74345`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652e2dc1413588e623e18b712880047f39297cc468a08211cafdb8e384ed807`  
		Last Modified: Thu, 02 Oct 2025 08:43:05 GMT  
		Size: 28.0 MB (27998640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6ab5b327b6bd6047607329f6741b3a38ecfaf409b4be319fe41d3bb611167e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f2048fc8bd5a8f2e9d68ea9921978ee8a2363108eb9ebb81683e652b3e7e5b`

```dockerfile
```

-	Layers:
	-	`sha256:73e777a6ccf4e32505263cf2bf6511bd5fb3e67a28d20ade0fc1f0a604c8b089`  
		Last Modified: Thu, 02 Oct 2025 10:17:36 GMT  
		Size: 24.5 MB (24543454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc5faa4f50770c1503c4f2512ad8317ee2e0a249f136176757377dc1d82c04`  
		Last Modified: Thu, 02 Oct 2025 10:17:37 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d0e5b652b7bc395b79e6bff9e10e35e862a5adfc7ebd756d0a198faa2c0eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286576562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b913ca6da461594facd10ff82b6ea5e40e574b18ceec831c3b7ad5673dc06f52`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c2f7c6c797eea4625f53276251170cff19433ffb3f5e9e3c53284d3f2efb08c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24582540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff22f022cce7b94679cd1f691bf2f478261c95ef41fc1f7b39d4905082e987e`

```dockerfile
```

-	Layers:
	-	`sha256:36155c38a5edb438516abb1f20660b99bbc32576ac6b765d7e5c63706c578e5c`  
		Last Modified: Thu, 02 Oct 2025 04:18:05 GMT  
		Size: 24.6 MB (24565727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f26318a42f5ecbcc048c1478bffee73eb09c82fdf00ce4c1242b859c846482`  
		Last Modified: Thu, 02 Oct 2025 04:18:06 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:4f2536852c6771406708e351858c2b3d0b1f9ad628278c33ecb179f9dcf4ad5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:b562f956fc138f4741ef99a7ec7da6cb207f968ad78431481e76ae3827572568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157358498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27aa14f9b6c9b89befea3bcdc02299c8458b975d6c04dcfd0d4a3f59ab815f0f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108b0455d26874467bb535ac1b0fb32de8c484d3ffd3710dbea124ffc245adb`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 120.1 MB (120110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d51c9d4c4e7ee2f490765efc765899f07ad09fdba245ea055344af0b2e9f2d`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:5b70d0eb9d9656cd82057b9c5c9b3aaa73d7df9716c946e4221433c9c0d6df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18314538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e518a419ab6d84ad80b001b66f7eca9181a9e0554d3c132a959c8c3b980d6`

```dockerfile
```

-	Layers:
	-	`sha256:745c761d3615d3a2597c85d87c43733490c1102be429cfabbe2bfc96f682f38d`  
		Last Modified: Fri, 10 Oct 2025 01:17:52 GMT  
		Size: 18.3 MB (18299895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0abe9db77d50e2e696d7fd5d096dc5018e2dac7548662f4bd8f3cf65ec5b4b7`  
		Last Modified: Fri, 10 Oct 2025 01:17:54 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5102a569630d1391222b5aa6ef6e0ccdca9a4775291abbf4f422de5954103ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151294155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8210fa0488361c2267050d8d5e72d5051ab64916ddf394571840c765afa3794`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb091d265588996d309a696050b8d873efa1a977c33604e5241d0745dae157`  
		Last Modified: Thu, 09 Oct 2025 21:26:15 GMT  
		Size: 114.9 MB (114893499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fd8e39aed1e99b329b904170291216c4df87e9a05ceb6e27c4e277cef7e6e`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4495fd35e1ec208fee280e5d5ce58c24feafb4f655f933c5e54e57f6df389bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18288669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82891b0d2625a4b9962d02deb7490ce3e320cf12a30b7161d0e966c3f2ee21f1`

```dockerfile
```

-	Layers:
	-	`sha256:cf09b7b71608b18f11fcf31d98f8974a7d9498198841cc56c43e1fc39e77a2ec`  
		Last Modified: Thu, 09 Oct 2025 21:24:10 GMT  
		Size: 18.3 MB (18273901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989bbd24ee2de74d927a6538ae8f557fcde6bfafcf6ec9ca08f5fc05379233be`  
		Last Modified: Thu, 09 Oct 2025 22:18:41 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:4f2536852c6771406708e351858c2b3d0b1f9ad628278c33ecb179f9dcf4ad5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:b562f956fc138f4741ef99a7ec7da6cb207f968ad78431481e76ae3827572568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157358498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27aa14f9b6c9b89befea3bcdc02299c8458b975d6c04dcfd0d4a3f59ab815f0f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108b0455d26874467bb535ac1b0fb32de8c484d3ffd3710dbea124ffc245adb`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 120.1 MB (120110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d51c9d4c4e7ee2f490765efc765899f07ad09fdba245ea055344af0b2e9f2d`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5b70d0eb9d9656cd82057b9c5c9b3aaa73d7df9716c946e4221433c9c0d6df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18314538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e518a419ab6d84ad80b001b66f7eca9181a9e0554d3c132a959c8c3b980d6`

```dockerfile
```

-	Layers:
	-	`sha256:745c761d3615d3a2597c85d87c43733490c1102be429cfabbe2bfc96f682f38d`  
		Last Modified: Fri, 10 Oct 2025 01:17:52 GMT  
		Size: 18.3 MB (18299895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0abe9db77d50e2e696d7fd5d096dc5018e2dac7548662f4bd8f3cf65ec5b4b7`  
		Last Modified: Fri, 10 Oct 2025 01:17:54 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5102a569630d1391222b5aa6ef6e0ccdca9a4775291abbf4f422de5954103ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151294155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8210fa0488361c2267050d8d5e72d5051ab64916ddf394571840c765afa3794`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb091d265588996d309a696050b8d873efa1a977c33604e5241d0745dae157`  
		Last Modified: Thu, 09 Oct 2025 21:26:15 GMT  
		Size: 114.9 MB (114893499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fd8e39aed1e99b329b904170291216c4df87e9a05ceb6e27c4e277cef7e6e`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4495fd35e1ec208fee280e5d5ce58c24feafb4f655f933c5e54e57f6df389bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18288669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82891b0d2625a4b9962d02deb7490ce3e320cf12a30b7161d0e966c3f2ee21f1`

```dockerfile
```

-	Layers:
	-	`sha256:cf09b7b71608b18f11fcf31d98f8974a7d9498198841cc56c43e1fc39e77a2ec`  
		Last Modified: Thu, 09 Oct 2025 21:24:10 GMT  
		Size: 18.3 MB (18273901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989bbd24ee2de74d927a6538ae8f557fcde6bfafcf6ec9ca08f5fc05379233be`  
		Last Modified: Thu, 09 Oct 2025 22:18:41 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:d4cb6579fd941a75b04edccfdb308270e4f98f6f006dddc218de080dafd4c2d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:d8198dfd872bb8ec331931325e04fdef44cd9d84a08d5525fe8387f11066c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313233194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55498ab711c0da96547ab0b20755452e54f40455a89db5534862b36ecd17e7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11ad22aa215c08ab1ddd8afcf87b3fa553117dd34ee4667c1b976a3cba5c61`  
		Last Modified: Thu, 02 Oct 2025 06:28:42 GMT  
		Size: 683.9 KB (683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e123d6ddecce0d115e4e5410f78a0f72324f8a035468137b9ee1364c334df2`  
		Last Modified: Thu, 02 Oct 2025 07:41:05 GMT  
		Size: 9.1 MB (9147619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567e6c6a0bca7204e8091a90278f279084d427cf99bcacb4c36bb80b4860ba9`  
		Last Modified: Thu, 02 Oct 2025 07:02:32 GMT  
		Size: 94.2 KB (94205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf308a9b4ee769ffe671af02237428bbea707579aa9053eec48de01d5691165`  
		Last Modified: Thu, 02 Oct 2025 08:40:38 GMT  
		Size: 135.0 MB (134982262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f34280af7632305bf440a28b5c441aa18ec0b5b665cb07eb7c5650b7e2267`  
		Last Modified: Thu, 02 Oct 2025 06:30:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66d21c8232d8783a7e2705dcddc210613500a4b975935094f13e8082d289c9a`  
		Last Modified: Thu, 02 Oct 2025 08:43:14 GMT  
		Size: 110.2 MB (110185711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760c71521ea26184b0599cdcba9130630299976a0ed74d9afcf9d6a379736d2`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5588a5d3ef0a80619aef78ff285dde481841fa73fafc364a7128c81f2ef933a`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb14e2f9ab03b3ce4945152457991029f211759a81f65e4a067268860e47c1`  
		Last Modified: Thu, 02 Oct 2025 08:43:06 GMT  
		Size: 28.1 MB (28051331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:809113821937da0dc60e2148f8f321ae6647cbd9fa2233743a2328eba9a6c638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c91bc257e8f6cf93fde475a1a7a86d09370d9234817ee1652ada18413ecac06`

```dockerfile
```

-	Layers:
	-	`sha256:26708050bd0233d66da04b64d875dbbd2a5b25beab6026f31a89eca93d1d16bf`  
		Last Modified: Thu, 02 Oct 2025 10:17:43 GMT  
		Size: 24.7 MB (24650296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1411a7d6fb3101893cc321b98ad7a67f34574a194ea33e07369e6caaa59f29`  
		Last Modified: Thu, 02 Oct 2025 10:17:44 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b35fc8a894c495bcf8272f81fd58405a84e6a4d9b76c5ff2eba8d7596998ff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301412796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd65f1dab0c81523927fc539ceec4bf3d110827c2c09c5e4bdae3ed6b8a1ace5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:6143c729057d88972ef32743622fc7039aa28ec23054b4b93fff4e2c74e3d0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4c790cb1b8298ff2fa1073c9e44999f84d254b87837aebd9117f973b9af2af`

```dockerfile
```

-	Layers:
	-	`sha256:ba3c600f8b51ff0cd430170467790fd36d876d4cec25414b9d2e1f3d53858214`  
		Last Modified: Thu, 02 Oct 2025 04:18:32 GMT  
		Size: 24.7 MB (24672557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e26b84d59d2f219bdc05e27305409e4821e848d7990978b2313b97ba9ce584`  
		Last Modified: Thu, 02 Oct 2025 04:18:33 GMT  
		Size: 16.5 KB (16526 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:f338af006d456dd4b9919504252eefb8ca4f1eff57b5ed5cbdbc47e177bf3463
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:53d3ccddb6e2b31d36bc45df90af638212f621afa1fb24acbb99406c95582122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1098205741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ace56c9751862d4973a146424025f4039ad7c8676e156feee8346da6b2634e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11ad22aa215c08ab1ddd8afcf87b3fa553117dd34ee4667c1b976a3cba5c61`  
		Last Modified: Thu, 02 Oct 2025 06:28:42 GMT  
		Size: 683.9 KB (683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e123d6ddecce0d115e4e5410f78a0f72324f8a035468137b9ee1364c334df2`  
		Last Modified: Thu, 02 Oct 2025 07:41:05 GMT  
		Size: 9.1 MB (9147619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567e6c6a0bca7204e8091a90278f279084d427cf99bcacb4c36bb80b4860ba9`  
		Last Modified: Thu, 02 Oct 2025 07:02:32 GMT  
		Size: 94.2 KB (94205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf308a9b4ee769ffe671af02237428bbea707579aa9053eec48de01d5691165`  
		Last Modified: Thu, 02 Oct 2025 08:40:38 GMT  
		Size: 135.0 MB (134982262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f34280af7632305bf440a28b5c441aa18ec0b5b665cb07eb7c5650b7e2267`  
		Last Modified: Thu, 02 Oct 2025 06:30:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66d21c8232d8783a7e2705dcddc210613500a4b975935094f13e8082d289c9a`  
		Last Modified: Thu, 02 Oct 2025 08:43:14 GMT  
		Size: 110.2 MB (110185711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760c71521ea26184b0599cdcba9130630299976a0ed74d9afcf9d6a379736d2`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5588a5d3ef0a80619aef78ff285dde481841fa73fafc364a7128c81f2ef933a`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb14e2f9ab03b3ce4945152457991029f211759a81f65e4a067268860e47c1`  
		Last Modified: Thu, 02 Oct 2025 08:43:06 GMT  
		Size: 28.1 MB (28051331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c3127fbcff76719a7f13056727bbb20c5828a27e14688ff7ec623538200256`  
		Last Modified: Thu, 02 Oct 2025 20:36:49 GMT  
		Size: 785.0 MB (784972547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:33af5c77568c8981fe0a074c3dfd26cc9a8ff16a901c3ffe4e562992d3e2fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8173db8583e3d6dae29d67deb6982b1edda12448ec94acae74083288f4915`

```dockerfile
```

-	Layers:
	-	`sha256:168067b7930ec0bffd26d93e056c06a7b840f6524b192dc866d126776c60bf21`  
		Last Modified: Thu, 02 Oct 2025 13:18:06 GMT  
		Size: 60.8 MB (60822377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db91243f3a26f5304aea14b6fcd8d4cc510ac5606b84c294bd942ad8217355a`  
		Last Modified: Thu, 02 Oct 2025 13:18:09 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b299f5123149caf8c27b4738218ddfad816b06629f06f8b23981b0f702127dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.4 MB (996376178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899ac3d335fcfb30f59981d69869304c7dcf53f08053d27dd420aa699f6dae9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e10717649fb04c0c45c9989ca7cbb84576448290e0f3d1a703166ec01d39ce`  
		Last Modified: Thu, 02 Oct 2025 06:35:22 GMT  
		Size: 695.0 MB (694963382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3cb719f408a19b8961f7a8a5329e20d4e07c0db664928ae14b9ccb01a88385fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f626ac4227909bc7adfff7d3e289c9b2ebcfdfa5425cdf374c694be2f8dd6`

```dockerfile
```

-	Layers:
	-	`sha256:d312e4430c740b516eec05d3643f0b9f1e58bad9e0bb37af1c9a7798ac98e519`  
		Last Modified: Thu, 02 Oct 2025 04:20:45 GMT  
		Size: 60.8 MB (60752902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a181c206ec07fdd0171e29a034af3ebf0d0614262b6562e8f08edeac22dea00`  
		Last Modified: Thu, 02 Oct 2025 04:20:46 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:f338af006d456dd4b9919504252eefb8ca4f1eff57b5ed5cbdbc47e177bf3463
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:53d3ccddb6e2b31d36bc45df90af638212f621afa1fb24acbb99406c95582122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1098205741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ace56c9751862d4973a146424025f4039ad7c8676e156feee8346da6b2634e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11ad22aa215c08ab1ddd8afcf87b3fa553117dd34ee4667c1b976a3cba5c61`  
		Last Modified: Thu, 02 Oct 2025 06:28:42 GMT  
		Size: 683.9 KB (683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e123d6ddecce0d115e4e5410f78a0f72324f8a035468137b9ee1364c334df2`  
		Last Modified: Thu, 02 Oct 2025 07:41:05 GMT  
		Size: 9.1 MB (9147619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567e6c6a0bca7204e8091a90278f279084d427cf99bcacb4c36bb80b4860ba9`  
		Last Modified: Thu, 02 Oct 2025 07:02:32 GMT  
		Size: 94.2 KB (94205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf308a9b4ee769ffe671af02237428bbea707579aa9053eec48de01d5691165`  
		Last Modified: Thu, 02 Oct 2025 08:40:38 GMT  
		Size: 135.0 MB (134982262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f34280af7632305bf440a28b5c441aa18ec0b5b665cb07eb7c5650b7e2267`  
		Last Modified: Thu, 02 Oct 2025 06:30:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66d21c8232d8783a7e2705dcddc210613500a4b975935094f13e8082d289c9a`  
		Last Modified: Thu, 02 Oct 2025 08:43:14 GMT  
		Size: 110.2 MB (110185711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760c71521ea26184b0599cdcba9130630299976a0ed74d9afcf9d6a379736d2`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5588a5d3ef0a80619aef78ff285dde481841fa73fafc364a7128c81f2ef933a`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb14e2f9ab03b3ce4945152457991029f211759a81f65e4a067268860e47c1`  
		Last Modified: Thu, 02 Oct 2025 08:43:06 GMT  
		Size: 28.1 MB (28051331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c3127fbcff76719a7f13056727bbb20c5828a27e14688ff7ec623538200256`  
		Last Modified: Thu, 02 Oct 2025 20:36:49 GMT  
		Size: 785.0 MB (784972547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:33af5c77568c8981fe0a074c3dfd26cc9a8ff16a901c3ffe4e562992d3e2fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8173db8583e3d6dae29d67deb6982b1edda12448ec94acae74083288f4915`

```dockerfile
```

-	Layers:
	-	`sha256:168067b7930ec0bffd26d93e056c06a7b840f6524b192dc866d126776c60bf21`  
		Last Modified: Thu, 02 Oct 2025 13:18:06 GMT  
		Size: 60.8 MB (60822377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db91243f3a26f5304aea14b6fcd8d4cc510ac5606b84c294bd942ad8217355a`  
		Last Modified: Thu, 02 Oct 2025 13:18:09 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b299f5123149caf8c27b4738218ddfad816b06629f06f8b23981b0f702127dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.4 MB (996376178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899ac3d335fcfb30f59981d69869304c7dcf53f08053d27dd420aa699f6dae9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e10717649fb04c0c45c9989ca7cbb84576448290e0f3d1a703166ec01d39ce`  
		Last Modified: Thu, 02 Oct 2025 06:35:22 GMT  
		Size: 695.0 MB (694963382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3cb719f408a19b8961f7a8a5329e20d4e07c0db664928ae14b9ccb01a88385fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f626ac4227909bc7adfff7d3e289c9b2ebcfdfa5425cdf374c694be2f8dd6`

```dockerfile
```

-	Layers:
	-	`sha256:d312e4430c740b516eec05d3643f0b9f1e58bad9e0bb37af1c9a7798ac98e519`  
		Last Modified: Thu, 02 Oct 2025 04:20:45 GMT  
		Size: 60.8 MB (60752902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a181c206ec07fdd0171e29a034af3ebf0d0614262b6562e8f08edeac22dea00`  
		Last Modified: Thu, 02 Oct 2025 04:20:46 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:d4cb6579fd941a75b04edccfdb308270e4f98f6f006dddc218de080dafd4c2d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d8198dfd872bb8ec331931325e04fdef44cd9d84a08d5525fe8387f11066c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313233194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55498ab711c0da96547ab0b20755452e54f40455a89db5534862b36ecd17e7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11ad22aa215c08ab1ddd8afcf87b3fa553117dd34ee4667c1b976a3cba5c61`  
		Last Modified: Thu, 02 Oct 2025 06:28:42 GMT  
		Size: 683.9 KB (683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e123d6ddecce0d115e4e5410f78a0f72324f8a035468137b9ee1364c334df2`  
		Last Modified: Thu, 02 Oct 2025 07:41:05 GMT  
		Size: 9.1 MB (9147619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567e6c6a0bca7204e8091a90278f279084d427cf99bcacb4c36bb80b4860ba9`  
		Last Modified: Thu, 02 Oct 2025 07:02:32 GMT  
		Size: 94.2 KB (94205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf308a9b4ee769ffe671af02237428bbea707579aa9053eec48de01d5691165`  
		Last Modified: Thu, 02 Oct 2025 08:40:38 GMT  
		Size: 135.0 MB (134982262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f34280af7632305bf440a28b5c441aa18ec0b5b665cb07eb7c5650b7e2267`  
		Last Modified: Thu, 02 Oct 2025 06:30:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66d21c8232d8783a7e2705dcddc210613500a4b975935094f13e8082d289c9a`  
		Last Modified: Thu, 02 Oct 2025 08:43:14 GMT  
		Size: 110.2 MB (110185711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760c71521ea26184b0599cdcba9130630299976a0ed74d9afcf9d6a379736d2`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5588a5d3ef0a80619aef78ff285dde481841fa73fafc364a7128c81f2ef933a`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb14e2f9ab03b3ce4945152457991029f211759a81f65e4a067268860e47c1`  
		Last Modified: Thu, 02 Oct 2025 08:43:06 GMT  
		Size: 28.1 MB (28051331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:809113821937da0dc60e2148f8f321ae6647cbd9fa2233743a2328eba9a6c638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c91bc257e8f6cf93fde475a1a7a86d09370d9234817ee1652ada18413ecac06`

```dockerfile
```

-	Layers:
	-	`sha256:26708050bd0233d66da04b64d875dbbd2a5b25beab6026f31a89eca93d1d16bf`  
		Last Modified: Thu, 02 Oct 2025 10:17:43 GMT  
		Size: 24.7 MB (24650296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1411a7d6fb3101893cc321b98ad7a67f34574a194ea33e07369e6caaa59f29`  
		Last Modified: Thu, 02 Oct 2025 10:17:44 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b35fc8a894c495bcf8272f81fd58405a84e6a4d9b76c5ff2eba8d7596998ff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301412796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd65f1dab0c81523927fc539ceec4bf3d110827c2c09c5e4bdae3ed6b8a1ace5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6143c729057d88972ef32743622fc7039aa28ec23054b4b93fff4e2c74e3d0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4c790cb1b8298ff2fa1073c9e44999f84d254b87837aebd9117f973b9af2af`

```dockerfile
```

-	Layers:
	-	`sha256:ba3c600f8b51ff0cd430170467790fd36d876d4cec25414b9d2e1f3d53858214`  
		Last Modified: Thu, 02 Oct 2025 04:18:32 GMT  
		Size: 24.7 MB (24672557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e26b84d59d2f219bdc05e27305409e4821e848d7990978b2313b97ba9ce584`  
		Last Modified: Thu, 02 Oct 2025 04:18:33 GMT  
		Size: 16.5 KB (16526 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:d4cb6579fd941a75b04edccfdb308270e4f98f6f006dddc218de080dafd4c2d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d8198dfd872bb8ec331931325e04fdef44cd9d84a08d5525fe8387f11066c067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313233194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55498ab711c0da96547ab0b20755452e54f40455a89db5534862b36ecd17e7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11ad22aa215c08ab1ddd8afcf87b3fa553117dd34ee4667c1b976a3cba5c61`  
		Last Modified: Thu, 02 Oct 2025 06:28:42 GMT  
		Size: 683.9 KB (683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e123d6ddecce0d115e4e5410f78a0f72324f8a035468137b9ee1364c334df2`  
		Last Modified: Thu, 02 Oct 2025 07:41:05 GMT  
		Size: 9.1 MB (9147619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567e6c6a0bca7204e8091a90278f279084d427cf99bcacb4c36bb80b4860ba9`  
		Last Modified: Thu, 02 Oct 2025 07:02:32 GMT  
		Size: 94.2 KB (94205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf308a9b4ee769ffe671af02237428bbea707579aa9053eec48de01d5691165`  
		Last Modified: Thu, 02 Oct 2025 08:40:38 GMT  
		Size: 135.0 MB (134982262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f34280af7632305bf440a28b5c441aa18ec0b5b665cb07eb7c5650b7e2267`  
		Last Modified: Thu, 02 Oct 2025 06:30:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66d21c8232d8783a7e2705dcddc210613500a4b975935094f13e8082d289c9a`  
		Last Modified: Thu, 02 Oct 2025 08:43:14 GMT  
		Size: 110.2 MB (110185711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760c71521ea26184b0599cdcba9130630299976a0ed74d9afcf9d6a379736d2`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5588a5d3ef0a80619aef78ff285dde481841fa73fafc364a7128c81f2ef933a`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb14e2f9ab03b3ce4945152457991029f211759a81f65e4a067268860e47c1`  
		Last Modified: Thu, 02 Oct 2025 08:43:06 GMT  
		Size: 28.1 MB (28051331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:809113821937da0dc60e2148f8f321ae6647cbd9fa2233743a2328eba9a6c638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c91bc257e8f6cf93fde475a1a7a86d09370d9234817ee1652ada18413ecac06`

```dockerfile
```

-	Layers:
	-	`sha256:26708050bd0233d66da04b64d875dbbd2a5b25beab6026f31a89eca93d1d16bf`  
		Last Modified: Thu, 02 Oct 2025 10:17:43 GMT  
		Size: 24.7 MB (24650296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1411a7d6fb3101893cc321b98ad7a67f34574a194ea33e07369e6caaa59f29`  
		Last Modified: Thu, 02 Oct 2025 10:17:44 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b35fc8a894c495bcf8272f81fd58405a84e6a4d9b76c5ff2eba8d7596998ff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301412796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd65f1dab0c81523927fc539ceec4bf3d110827c2c09c5e4bdae3ed6b8a1ace5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6143c729057d88972ef32743622fc7039aa28ec23054b4b93fff4e2c74e3d0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4c790cb1b8298ff2fa1073c9e44999f84d254b87837aebd9117f973b9af2af`

```dockerfile
```

-	Layers:
	-	`sha256:ba3c600f8b51ff0cd430170467790fd36d876d4cec25414b9d2e1f3d53858214`  
		Last Modified: Thu, 02 Oct 2025 04:18:32 GMT  
		Size: 24.7 MB (24672557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e26b84d59d2f219bdc05e27305409e4821e848d7990978b2313b97ba9ce584`  
		Last Modified: Thu, 02 Oct 2025 04:18:33 GMT  
		Size: 16.5 KB (16526 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:2a5a0f80fb950bcd79720f1f3e3ae91e38487b5ac18ac168e5a5c34c40263215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f350c3d4f507a87bfb1fd30642463de061c33438dd8dc43b75e8a4da324ae198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172229902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13c7776c6db86aec9718e0b74f098f733da05df0710da9368fc38093b170b75`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad95cd04f77e0c5e96a8b537442f4b5d8be45febd447202f388d3a44663a30`  
		Last Modified: Thu, 09 Oct 2025 22:19:29 GMT  
		Size: 135.0 MB (134981480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b48f84fffbd5e61ea1d7e61e4143c8c98c1f4a0bff60b9411fd58aa4c63864`  
		Last Modified: Thu, 09 Oct 2025 21:25:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:9692c447c8b825099c0f96f6e365aaf59d03f9520bea79788d79a402f532d498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638bacd1f7a9b35ee59e98b486fa0b1dcfaf1f41087720db20c112b4659b6148`

```dockerfile
```

-	Layers:
	-	`sha256:9891b8f45133f25976c97df9943ea97919ff5420853d6f8387a250dd82a73aa4`  
		Last Modified: Fri, 10 Oct 2025 01:17:38 GMT  
		Size: 18.4 MB (18399851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc0c206e706d0a968c019d924567c807b85c5061d4776bd641b7d729025ab66e`  
		Last Modified: Fri, 10 Oct 2025 01:17:39 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a002c12d96b706ffbc2430ad3d0a8e5562b8507d9cc3f1acc3d7044ad80ffd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166104217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dce02b7ce5c48a46e237aeede4ccb8dbb113a66f7999ee2fc0303c9e2f716f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f2e5bdb9ebc2dd1e4a97e4c4f8f6a4caa1a8d2b8c88779e314bfedf21b5eb`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431df98e5fde48f4218abb39181387c9329df717368142b9f365818c84a2731`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283f352fd757879170ef433d2bc7b2b87844a7e64a56c215fd7e8bcf52511b33`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf903136d1425abdcfe45e487f28e07cfa1010e029bb0e9ea8ac6096c30939`  
		Last Modified: Thu, 09 Oct 2025 22:19:34 GMT  
		Size: 129.7 MB (129703599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680295d190e67764ff4359841a9d2f64ece12ca1088d22d70f40d69e908a05fc`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:8b2860c1621b703d8ce45eb6fc0e6f79f365f14ba2eabc712ebea7ce14568400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89b421b8535aba4924b4910e4b2800e3600538d6bb91f2ffe9bcba4b12f4c8`

```dockerfile
```

-	Layers:
	-	`sha256:17a970e5b5e850925606b2669971db1122a3a88e6b420328a58e045438ad354d`  
		Last Modified: Fri, 10 Oct 2025 01:17:56 GMT  
		Size: 18.4 MB (18373857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60eec2f4ecfdb667a440a1de8e5abc0871e69aed85644eca4084504fce0847c8`  
		Last Modified: Fri, 10 Oct 2025 01:17:57 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:2a5a0f80fb950bcd79720f1f3e3ae91e38487b5ac18ac168e5a5c34c40263215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:f350c3d4f507a87bfb1fd30642463de061c33438dd8dc43b75e8a4da324ae198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172229902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13c7776c6db86aec9718e0b74f098f733da05df0710da9368fc38093b170b75`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad95cd04f77e0c5e96a8b537442f4b5d8be45febd447202f388d3a44663a30`  
		Last Modified: Thu, 09 Oct 2025 22:19:29 GMT  
		Size: 135.0 MB (134981480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b48f84fffbd5e61ea1d7e61e4143c8c98c1f4a0bff60b9411fd58aa4c63864`  
		Last Modified: Thu, 09 Oct 2025 21:25:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9692c447c8b825099c0f96f6e365aaf59d03f9520bea79788d79a402f532d498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638bacd1f7a9b35ee59e98b486fa0b1dcfaf1f41087720db20c112b4659b6148`

```dockerfile
```

-	Layers:
	-	`sha256:9891b8f45133f25976c97df9943ea97919ff5420853d6f8387a250dd82a73aa4`  
		Last Modified: Fri, 10 Oct 2025 01:17:38 GMT  
		Size: 18.4 MB (18399851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc0c206e706d0a968c019d924567c807b85c5061d4776bd641b7d729025ab66e`  
		Last Modified: Fri, 10 Oct 2025 01:17:39 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a002c12d96b706ffbc2430ad3d0a8e5562b8507d9cc3f1acc3d7044ad80ffd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166104217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dce02b7ce5c48a46e237aeede4ccb8dbb113a66f7999ee2fc0303c9e2f716f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f2e5bdb9ebc2dd1e4a97e4c4f8f6a4caa1a8d2b8c88779e314bfedf21b5eb`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431df98e5fde48f4218abb39181387c9329df717368142b9f365818c84a2731`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283f352fd757879170ef433d2bc7b2b87844a7e64a56c215fd7e8bcf52511b33`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf903136d1425abdcfe45e487f28e07cfa1010e029bb0e9ea8ac6096c30939`  
		Last Modified: Thu, 09 Oct 2025 22:19:34 GMT  
		Size: 129.7 MB (129703599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680295d190e67764ff4359841a9d2f64ece12ca1088d22d70f40d69e908a05fc`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8b2860c1621b703d8ce45eb6fc0e6f79f365f14ba2eabc712ebea7ce14568400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89b421b8535aba4924b4910e4b2800e3600538d6bb91f2ffe9bcba4b12f4c8`

```dockerfile
```

-	Layers:
	-	`sha256:17a970e5b5e850925606b2669971db1122a3a88e6b420328a58e045438ad354d`  
		Last Modified: Fri, 10 Oct 2025 01:17:56 GMT  
		Size: 18.4 MB (18373857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60eec2f4ecfdb667a440a1de8e5abc0871e69aed85644eca4084504fce0847c8`  
		Last Modified: Fri, 10 Oct 2025 01:17:57 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:6616419d6752d8ef5822f774332a6d845ef909b9f28454428b4dadacf83f4d6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:21ca684a69663bce262ef38b418ceff778dc8d056d69fc9cdfe3b165a4f79baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298320939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94767efcadc98a9f3ba867d6e5393774aa6b16b0acdc42c7fc8fa71b096a9125`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8bb927407dff4c86a177c9405741da663a12e7437133c81c62c81e2449e128`  
		Last Modified: Thu, 02 Oct 2025 05:18:07 GMT  
		Size: 683.9 KB (683867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fd9f21b79e9e7e0ad635ba1a0a6b43c12e475289642f226f9e319bd5ea695d`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 9.1 MB (9147634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611dec3b085de3fbf3f81cbb44b6455eb23dc88e6dc09b64612a281b23cc9503`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 94.2 KB (94194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1860cf45bc9590dfdc2f85a44991d355a3ea1a413aee3c6e1d492d14f4c3aa61`  
		Last Modified: Thu, 02 Oct 2025 05:18:21 GMT  
		Size: 120.1 MB (120110330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966aa943b4b80bfd43fd9d346c621bb5e892b996fbafb736be801a8cffb8c533`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0db01ed68fe206c42cfc647439c7dc83490be9f02d80f59772c0dbdf465c0f`  
		Last Modified: Thu, 02 Oct 2025 08:43:08 GMT  
		Size: 110.2 MB (110182298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c7f1f3966277d41eed6bc49ebec744e08dad8b9fee5c18c228ca040a514c`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56e56c16231d651035aa39e28cdadcd9a7944f8fd4121a0ce2e4d572c74345`  
		Last Modified: Thu, 02 Oct 2025 08:42:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5652e2dc1413588e623e18b712880047f39297cc468a08211cafdb8e384ed807`  
		Last Modified: Thu, 02 Oct 2025 08:43:05 GMT  
		Size: 28.0 MB (27998640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:6ab5b327b6bd6047607329f6741b3a38ecfaf409b4be319fe41d3bb611167e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f2048fc8bd5a8f2e9d68ea9921978ee8a2363108eb9ebb81683e652b3e7e5b`

```dockerfile
```

-	Layers:
	-	`sha256:73e777a6ccf4e32505263cf2bf6511bd5fb3e67a28d20ade0fc1f0a604c8b089`  
		Last Modified: Thu, 02 Oct 2025 10:17:36 GMT  
		Size: 24.5 MB (24543454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfc5faa4f50770c1503c4f2512ad8317ee2e0a249f136176757377dc1d82c04`  
		Last Modified: Thu, 02 Oct 2025 10:17:37 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d0e5b652b7bc395b79e6bff9e10e35e862a5adfc7ebd756d0a198faa2c0eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286576562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b913ca6da461594facd10ff82b6ea5e40e574b18ceec831c3b7ad5673dc06f52`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:c2f7c6c797eea4625f53276251170cff19433ffb3f5e9e3c53284d3f2efb08c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24582540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff22f022cce7b94679cd1f691bf2f478261c95ef41fc1f7b39d4905082e987e`

```dockerfile
```

-	Layers:
	-	`sha256:36155c38a5edb438516abb1f20660b99bbc32576ac6b765d7e5c63706c578e5c`  
		Last Modified: Thu, 02 Oct 2025 04:18:05 GMT  
		Size: 24.6 MB (24565727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f26318a42f5ecbcc048c1478bffee73eb09c82fdf00ce4c1242b859c846482`  
		Last Modified: Thu, 02 Oct 2025 04:18:06 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:07fd9dfe3508c287cc9994f40e62909b6345449ace249122877a43c16853cfff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:86e0502e7e2e95558bcbae65aace7babcf8771dc70414c9ecee41509f99c0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327051743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65668ce64c9c8468d936f1af5b60d1326cf1c52a8490bf6dd81ee6e5b57ccfc6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61cd581a56f484742941f9fecb044c9b59058d2fa4beedf24f7e7885f01d23`  
		Last Modified: Thu, 02 Oct 2025 06:28:54 GMT  
		Size: 683.9 KB (683878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171251c304424eb6f36b5385f9d7d05b22608afe36a4d7218e9d8cb3ca31479`  
		Last Modified: Thu, 02 Oct 2025 07:40:58 GMT  
		Size: 9.1 MB (9147633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ffa5de5de694e11dd8fab9a66b88aee908fd14c9f86af59376c5b570314a9`  
		Last Modified: Thu, 02 Oct 2025 06:29:01 GMT  
		Size: 94.2 KB (94202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155f8d6d58365d02cbb1abdf9be88b90b2885ab7b839682ddf8c5af3e0c9fc2`  
		Last Modified: Thu, 02 Oct 2025 07:41:07 GMT  
		Size: 148.8 MB (148816264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce003c37d3b958571a9c710e8a9dc81cf1125c8483b6386a97293006bd747b`  
		Last Modified: Thu, 02 Oct 2025 06:29:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3311874e56d0a6824364bbac059cc43e6badf6eea3008cbee875737dcb636cb`  
		Last Modified: Thu, 02 Oct 2025 08:47:14 GMT  
		Size: 110.2 MB (110186692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2031436755676a305b3188c60bfddba85f5867de88dd480160afdd2928efb9a6`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 355.7 KB (355733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d23d85055afcc3c0e9479a1518fbca2c51ce686a5df837f9157160634b088`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200b3bdbe806fe52a8d0b156e38d69f34e2f262e9b309eb651e23165677498e`  
		Last Modified: Thu, 02 Oct 2025 08:47:11 GMT  
		Size: 28.0 MB (28041672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:1db20d590a2c850399a02493d2382c9e0e7f8d3166feb805c4e09dbaf4054b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25599452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157fd3e7108807a16680d79e6b9c3ad4933d262ded189b6e4a28e3720945007e`

```dockerfile
```

-	Layers:
	-	`sha256:66cf50c1c16cc6aa51c996649f98265113dd7116359a5249fb0808816d24a3c2`  
		Last Modified: Thu, 02 Oct 2025 10:17:58 GMT  
		Size: 25.6 MB (25583044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73f7fe9497433a0cf500a856cf20da1ac2968f96867d558cf4aa54b3d25f5e1`  
		Last Modified: Thu, 02 Oct 2025 10:17:59 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bf8df8af2693c9524125412c0513ca2f2aa7a3e8669f1f02ed9cd90cbbd0978e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314832345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2361206f4eb90de5ec0d3b984ec5ad5e7dc452683be75b3482b40cc1878089a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4867bbf27802ebcec126da4f4f575520a706c2de1b5cab1b07f4d8c8ce60ae4`  
		Last Modified: Thu, 02 Oct 2025 02:29:11 GMT  
		Size: 105.6 MB (105594631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a6d41bbeb02aaf40e3187214c2c70bea0c74ed6f768294ae35e88c75ba48`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 355.7 KB (355734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebae24cd02da0cf854a5ee1e08308bf6d2b3ad5b2375052e084657c981d1aa7`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829949e7504fb2923c21b6dba15e172d82d6a35d1f358470c866a163ff2b91a`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 27.1 MB (27123180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:9134bb428ed8a7b2074c9f77a0ce409207d8b50a9ca7a3ffe0f5d65741eec4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25622047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07770cac81e9cd393b90faff9c8b722e0f4252f55ef6d58b4ec9c4c4ee639fa6`

```dockerfile
```

-	Layers:
	-	`sha256:f0c5ee712074116e305cd84771afb611bab3a06b89250697a16b5e70aabc0316`  
		Last Modified: Thu, 02 Oct 2025 04:19:04 GMT  
		Size: 25.6 MB (25605502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58639b7ff5de7f8336e25023e740ccecc53d3843a6521d65388a2052ac9c28d`  
		Last Modified: Thu, 02 Oct 2025 04:19:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:e9939de0fd4fb6065494f12830a1fa1d030ec6fabf398b8fb87331e980e759b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:cf3e74c985260a0fcf4a1f5f0e121c74d0248a05217992f3e005b355542b0361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1111936049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8881edbed91c5eed923c596356ec3b576ec21f4e736f5063c71b19ec293afc8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61cd581a56f484742941f9fecb044c9b59058d2fa4beedf24f7e7885f01d23`  
		Last Modified: Thu, 02 Oct 2025 06:28:54 GMT  
		Size: 683.9 KB (683878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171251c304424eb6f36b5385f9d7d05b22608afe36a4d7218e9d8cb3ca31479`  
		Last Modified: Thu, 02 Oct 2025 07:40:58 GMT  
		Size: 9.1 MB (9147633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ffa5de5de694e11dd8fab9a66b88aee908fd14c9f86af59376c5b570314a9`  
		Last Modified: Thu, 02 Oct 2025 06:29:01 GMT  
		Size: 94.2 KB (94202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155f8d6d58365d02cbb1abdf9be88b90b2885ab7b839682ddf8c5af3e0c9fc2`  
		Last Modified: Thu, 02 Oct 2025 07:41:07 GMT  
		Size: 148.8 MB (148816264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce003c37d3b958571a9c710e8a9dc81cf1125c8483b6386a97293006bd747b`  
		Last Modified: Thu, 02 Oct 2025 06:29:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3311874e56d0a6824364bbac059cc43e6badf6eea3008cbee875737dcb636cb`  
		Last Modified: Thu, 02 Oct 2025 08:47:14 GMT  
		Size: 110.2 MB (110186692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2031436755676a305b3188c60bfddba85f5867de88dd480160afdd2928efb9a6`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 355.7 KB (355733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d23d85055afcc3c0e9479a1518fbca2c51ce686a5df837f9157160634b088`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200b3bdbe806fe52a8d0b156e38d69f34e2f262e9b309eb651e23165677498e`  
		Last Modified: Thu, 02 Oct 2025 08:47:11 GMT  
		Size: 28.0 MB (28041672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd1961ff94a232dfb0517663c2b3dcc652a33abf5d877df9ef159927270cbd2`  
		Last Modified: Thu, 02 Oct 2025 13:20:56 GMT  
		Size: 784.9 MB (784884306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0fbef80c39af9322714f74e36ae0b54f8f917a7f4db57c2b90fb45286bd306b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61765051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601af995edf12475577c2ab453eb06cf1155dd7e5648025a811d2d057b51b516`

```dockerfile
```

-	Layers:
	-	`sha256:9ca78e5544cdce49384bef0c4a4378f313044c7bd53f660def4677fabfcb2149`  
		Last Modified: Thu, 02 Oct 2025 13:18:16 GMT  
		Size: 61.8 MB (61755647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de263ef8dab896ad23482dc683da862b7ca4e2c3d8d3466008188a67d21a4d6d`  
		Last Modified: Thu, 02 Oct 2025 13:18:17 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d2f4d14a46ae5c7f5285d3b6dbdc70f9177b985dd6559f9da694fdaea229faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1009713604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be8d477d600961ba7b8225e29aecc15f0ab4f43b32b09815d25faa25aa87d90`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4867bbf27802ebcec126da4f4f575520a706c2de1b5cab1b07f4d8c8ce60ae4`  
		Last Modified: Thu, 02 Oct 2025 02:29:11 GMT  
		Size: 105.6 MB (105594631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a6d41bbeb02aaf40e3187214c2c70bea0c74ed6f768294ae35e88c75ba48`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 355.7 KB (355734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebae24cd02da0cf854a5ee1e08308bf6d2b3ad5b2375052e084657c981d1aa7`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829949e7504fb2923c21b6dba15e172d82d6a35d1f358470c866a163ff2b91a`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 27.1 MB (27123180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d527e4874e96a4508731ef6d33d6fafffdc92793ff47bdd173a276e7d4f968`  
		Last Modified: Thu, 02 Oct 2025 20:45:15 GMT  
		Size: 694.9 MB (694881259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0f760fdfcf698bc756fd491e90702d8e2c3570b37539de6ab2d0c480a6c1cae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61695853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666953a248101e452327a88733d4ed470158fcf8cbb113a80758faf807ecebdc`

```dockerfile
```

-	Layers:
	-	`sha256:af33cad7aac03a4d98b941153dd8842bf065c713d192ab9eff4ee87989a1dd8a`  
		Last Modified: Thu, 02 Oct 2025 04:20:38 GMT  
		Size: 61.7 MB (61686369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2aa219138327d20373bf98932a1cf501f8a72a44ea1de84f77b5dd81dbf670`  
		Last Modified: Thu, 02 Oct 2025 04:20:39 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:e9939de0fd4fb6065494f12830a1fa1d030ec6fabf398b8fb87331e980e759b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:cf3e74c985260a0fcf4a1f5f0e121c74d0248a05217992f3e005b355542b0361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1111936049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8881edbed91c5eed923c596356ec3b576ec21f4e736f5063c71b19ec293afc8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61cd581a56f484742941f9fecb044c9b59058d2fa4beedf24f7e7885f01d23`  
		Last Modified: Thu, 02 Oct 2025 06:28:54 GMT  
		Size: 683.9 KB (683878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171251c304424eb6f36b5385f9d7d05b22608afe36a4d7218e9d8cb3ca31479`  
		Last Modified: Thu, 02 Oct 2025 07:40:58 GMT  
		Size: 9.1 MB (9147633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ffa5de5de694e11dd8fab9a66b88aee908fd14c9f86af59376c5b570314a9`  
		Last Modified: Thu, 02 Oct 2025 06:29:01 GMT  
		Size: 94.2 KB (94202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155f8d6d58365d02cbb1abdf9be88b90b2885ab7b839682ddf8c5af3e0c9fc2`  
		Last Modified: Thu, 02 Oct 2025 07:41:07 GMT  
		Size: 148.8 MB (148816264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce003c37d3b958571a9c710e8a9dc81cf1125c8483b6386a97293006bd747b`  
		Last Modified: Thu, 02 Oct 2025 06:29:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3311874e56d0a6824364bbac059cc43e6badf6eea3008cbee875737dcb636cb`  
		Last Modified: Thu, 02 Oct 2025 08:47:14 GMT  
		Size: 110.2 MB (110186692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2031436755676a305b3188c60bfddba85f5867de88dd480160afdd2928efb9a6`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 355.7 KB (355733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d23d85055afcc3c0e9479a1518fbca2c51ce686a5df837f9157160634b088`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200b3bdbe806fe52a8d0b156e38d69f34e2f262e9b309eb651e23165677498e`  
		Last Modified: Thu, 02 Oct 2025 08:47:11 GMT  
		Size: 28.0 MB (28041672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd1961ff94a232dfb0517663c2b3dcc652a33abf5d877df9ef159927270cbd2`  
		Last Modified: Thu, 02 Oct 2025 13:20:56 GMT  
		Size: 784.9 MB (784884306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0fbef80c39af9322714f74e36ae0b54f8f917a7f4db57c2b90fb45286bd306b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61765051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601af995edf12475577c2ab453eb06cf1155dd7e5648025a811d2d057b51b516`

```dockerfile
```

-	Layers:
	-	`sha256:9ca78e5544cdce49384bef0c4a4378f313044c7bd53f660def4677fabfcb2149`  
		Last Modified: Thu, 02 Oct 2025 13:18:16 GMT  
		Size: 61.8 MB (61755647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de263ef8dab896ad23482dc683da862b7ca4e2c3d8d3466008188a67d21a4d6d`  
		Last Modified: Thu, 02 Oct 2025 13:18:17 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d2f4d14a46ae5c7f5285d3b6dbdc70f9177b985dd6559f9da694fdaea229faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1009713604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be8d477d600961ba7b8225e29aecc15f0ab4f43b32b09815d25faa25aa87d90`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4867bbf27802ebcec126da4f4f575520a706c2de1b5cab1b07f4d8c8ce60ae4`  
		Last Modified: Thu, 02 Oct 2025 02:29:11 GMT  
		Size: 105.6 MB (105594631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a6d41bbeb02aaf40e3187214c2c70bea0c74ed6f768294ae35e88c75ba48`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 355.7 KB (355734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebae24cd02da0cf854a5ee1e08308bf6d2b3ad5b2375052e084657c981d1aa7`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829949e7504fb2923c21b6dba15e172d82d6a35d1f358470c866a163ff2b91a`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 27.1 MB (27123180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d527e4874e96a4508731ef6d33d6fafffdc92793ff47bdd173a276e7d4f968`  
		Last Modified: Thu, 02 Oct 2025 20:45:15 GMT  
		Size: 694.9 MB (694881259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0f760fdfcf698bc756fd491e90702d8e2c3570b37539de6ab2d0c480a6c1cae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61695853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666953a248101e452327a88733d4ed470158fcf8cbb113a80758faf807ecebdc`

```dockerfile
```

-	Layers:
	-	`sha256:af33cad7aac03a4d98b941153dd8842bf065c713d192ab9eff4ee87989a1dd8a`  
		Last Modified: Thu, 02 Oct 2025 04:20:38 GMT  
		Size: 61.7 MB (61686369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2aa219138327d20373bf98932a1cf501f8a72a44ea1de84f77b5dd81dbf670`  
		Last Modified: Thu, 02 Oct 2025 04:20:39 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:07fd9dfe3508c287cc9994f40e62909b6345449ace249122877a43c16853cfff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:86e0502e7e2e95558bcbae65aace7babcf8771dc70414c9ecee41509f99c0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327051743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65668ce64c9c8468d936f1af5b60d1326cf1c52a8490bf6dd81ee6e5b57ccfc6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61cd581a56f484742941f9fecb044c9b59058d2fa4beedf24f7e7885f01d23`  
		Last Modified: Thu, 02 Oct 2025 06:28:54 GMT  
		Size: 683.9 KB (683878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171251c304424eb6f36b5385f9d7d05b22608afe36a4d7218e9d8cb3ca31479`  
		Last Modified: Thu, 02 Oct 2025 07:40:58 GMT  
		Size: 9.1 MB (9147633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ffa5de5de694e11dd8fab9a66b88aee908fd14c9f86af59376c5b570314a9`  
		Last Modified: Thu, 02 Oct 2025 06:29:01 GMT  
		Size: 94.2 KB (94202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155f8d6d58365d02cbb1abdf9be88b90b2885ab7b839682ddf8c5af3e0c9fc2`  
		Last Modified: Thu, 02 Oct 2025 07:41:07 GMT  
		Size: 148.8 MB (148816264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce003c37d3b958571a9c710e8a9dc81cf1125c8483b6386a97293006bd747b`  
		Last Modified: Thu, 02 Oct 2025 06:29:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3311874e56d0a6824364bbac059cc43e6badf6eea3008cbee875737dcb636cb`  
		Last Modified: Thu, 02 Oct 2025 08:47:14 GMT  
		Size: 110.2 MB (110186692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2031436755676a305b3188c60bfddba85f5867de88dd480160afdd2928efb9a6`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 355.7 KB (355733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d23d85055afcc3c0e9479a1518fbca2c51ce686a5df837f9157160634b088`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200b3bdbe806fe52a8d0b156e38d69f34e2f262e9b309eb651e23165677498e`  
		Last Modified: Thu, 02 Oct 2025 08:47:11 GMT  
		Size: 28.0 MB (28041672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:1db20d590a2c850399a02493d2382c9e0e7f8d3166feb805c4e09dbaf4054b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25599452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157fd3e7108807a16680d79e6b9c3ad4933d262ded189b6e4a28e3720945007e`

```dockerfile
```

-	Layers:
	-	`sha256:66cf50c1c16cc6aa51c996649f98265113dd7116359a5249fb0808816d24a3c2`  
		Last Modified: Thu, 02 Oct 2025 10:17:58 GMT  
		Size: 25.6 MB (25583044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73f7fe9497433a0cf500a856cf20da1ac2968f96867d558cf4aa54b3d25f5e1`  
		Last Modified: Thu, 02 Oct 2025 10:17:59 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bf8df8af2693c9524125412c0513ca2f2aa7a3e8669f1f02ed9cd90cbbd0978e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314832345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2361206f4eb90de5ec0d3b984ec5ad5e7dc452683be75b3482b40cc1878089a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4867bbf27802ebcec126da4f4f575520a706c2de1b5cab1b07f4d8c8ce60ae4`  
		Last Modified: Thu, 02 Oct 2025 02:29:11 GMT  
		Size: 105.6 MB (105594631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a6d41bbeb02aaf40e3187214c2c70bea0c74ed6f768294ae35e88c75ba48`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 355.7 KB (355734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebae24cd02da0cf854a5ee1e08308bf6d2b3ad5b2375052e084657c981d1aa7`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829949e7504fb2923c21b6dba15e172d82d6a35d1f358470c866a163ff2b91a`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 27.1 MB (27123180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9134bb428ed8a7b2074c9f77a0ce409207d8b50a9ca7a3ffe0f5d65741eec4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25622047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07770cac81e9cd393b90faff9c8b722e0f4252f55ef6d58b4ec9c4c4ee639fa6`

```dockerfile
```

-	Layers:
	-	`sha256:f0c5ee712074116e305cd84771afb611bab3a06b89250697a16b5e70aabc0316`  
		Last Modified: Thu, 02 Oct 2025 04:19:04 GMT  
		Size: 25.6 MB (25605502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58639b7ff5de7f8336e25023e740ccecc53d3843a6521d65388a2052ac9c28d`  
		Last Modified: Thu, 02 Oct 2025 04:19:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:07fd9dfe3508c287cc9994f40e62909b6345449ace249122877a43c16853cfff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:86e0502e7e2e95558bcbae65aace7babcf8771dc70414c9ecee41509f99c0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327051743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65668ce64c9c8468d936f1af5b60d1326cf1c52a8490bf6dd81ee6e5b57ccfc6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61cd581a56f484742941f9fecb044c9b59058d2fa4beedf24f7e7885f01d23`  
		Last Modified: Thu, 02 Oct 2025 06:28:54 GMT  
		Size: 683.9 KB (683878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171251c304424eb6f36b5385f9d7d05b22608afe36a4d7218e9d8cb3ca31479`  
		Last Modified: Thu, 02 Oct 2025 07:40:58 GMT  
		Size: 9.1 MB (9147633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ffa5de5de694e11dd8fab9a66b88aee908fd14c9f86af59376c5b570314a9`  
		Last Modified: Thu, 02 Oct 2025 06:29:01 GMT  
		Size: 94.2 KB (94202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155f8d6d58365d02cbb1abdf9be88b90b2885ab7b839682ddf8c5af3e0c9fc2`  
		Last Modified: Thu, 02 Oct 2025 07:41:07 GMT  
		Size: 148.8 MB (148816264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce003c37d3b958571a9c710e8a9dc81cf1125c8483b6386a97293006bd747b`  
		Last Modified: Thu, 02 Oct 2025 06:29:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3311874e56d0a6824364bbac059cc43e6badf6eea3008cbee875737dcb636cb`  
		Last Modified: Thu, 02 Oct 2025 08:47:14 GMT  
		Size: 110.2 MB (110186692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2031436755676a305b3188c60bfddba85f5867de88dd480160afdd2928efb9a6`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 355.7 KB (355733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d23d85055afcc3c0e9479a1518fbca2c51ce686a5df837f9157160634b088`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200b3bdbe806fe52a8d0b156e38d69f34e2f262e9b309eb651e23165677498e`  
		Last Modified: Thu, 02 Oct 2025 08:47:11 GMT  
		Size: 28.0 MB (28041672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1db20d590a2c850399a02493d2382c9e0e7f8d3166feb805c4e09dbaf4054b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25599452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157fd3e7108807a16680d79e6b9c3ad4933d262ded189b6e4a28e3720945007e`

```dockerfile
```

-	Layers:
	-	`sha256:66cf50c1c16cc6aa51c996649f98265113dd7116359a5249fb0808816d24a3c2`  
		Last Modified: Thu, 02 Oct 2025 10:17:58 GMT  
		Size: 25.6 MB (25583044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73f7fe9497433a0cf500a856cf20da1ac2968f96867d558cf4aa54b3d25f5e1`  
		Last Modified: Thu, 02 Oct 2025 10:17:59 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bf8df8af2693c9524125412c0513ca2f2aa7a3e8669f1f02ed9cd90cbbd0978e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314832345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2361206f4eb90de5ec0d3b984ec5ad5e7dc452683be75b3482b40cc1878089a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4867bbf27802ebcec126da4f4f575520a706c2de1b5cab1b07f4d8c8ce60ae4`  
		Last Modified: Thu, 02 Oct 2025 02:29:11 GMT  
		Size: 105.6 MB (105594631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a6d41bbeb02aaf40e3187214c2c70bea0c74ed6f768294ae35e88c75ba48`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 355.7 KB (355734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebae24cd02da0cf854a5ee1e08308bf6d2b3ad5b2375052e084657c981d1aa7`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829949e7504fb2923c21b6dba15e172d82d6a35d1f358470c866a163ff2b91a`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 27.1 MB (27123180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9134bb428ed8a7b2074c9f77a0ce409207d8b50a9ca7a3ffe0f5d65741eec4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25622047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07770cac81e9cd393b90faff9c8b722e0f4252f55ef6d58b4ec9c4c4ee639fa6`

```dockerfile
```

-	Layers:
	-	`sha256:f0c5ee712074116e305cd84771afb611bab3a06b89250697a16b5e70aabc0316`  
		Last Modified: Thu, 02 Oct 2025 04:19:04 GMT  
		Size: 25.6 MB (25605502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58639b7ff5de7f8336e25023e740ccecc53d3843a6521d65388a2052ac9c28d`  
		Last Modified: Thu, 02 Oct 2025 04:19:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:9a3ad210f7d02295b4d8ac56cec23c254ec53c1d0f620acbea649d15b3ec45b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:da420d243a5f5deec5501a795dcec056be107d4080bac2cc62680fe413736331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186062757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e95bb3ab43d416620b526087706fea37c9724a7ad23d2c39aaf36e61cfce2c2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081cac45e5fb7bc52c7bf496d2ccc3433f84dd8702adc9fa84d467cc2be5543`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb1361c757ec00d31a8c6c88058fd62b23da12af4290edf2d3b2c636f6da5a`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 6.7 MB (6746865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4540fb962b4d5de83708d3245134aac24f8adcb8d8457e317648dfe877db60`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 94.1 KB (94146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebe16a8832263871186c0dda7eaada9cdcfd4f1a4bcc90feccdb47acfff940`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 148.8 MB (148814487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda935e56c9a4a7f7f77e60fc31b89aa8dc68da689983df8cab450bf7bace1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:583945997ea59965ad3f4c7af3755f49f3658da3a092fb6c7fa0256b5cce262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19372017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde41f672c26b2756bcd8b10a33e18c6578776958d5d196d11efa808359a758d`

```dockerfile
```

-	Layers:
	-	`sha256:68c6611438f216e71285b4641824919748c76887cd70a29dc14cdb6c0499bea8`  
		Last Modified: Fri, 10 Oct 2025 01:17:51 GMT  
		Size: 19.4 MB (19357356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84946b9639aa950d309fda6bbfb20d1060f026e4f1e503028ec8f54814f3f48c`  
		Last Modified: Fri, 10 Oct 2025 01:17:52 GMT  
		Size: 14.7 KB (14661 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34933f25fb92bffb2a6fbf696e48dc327811da2099ac14a6873c9594b44aa9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179543247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf1df2b73e2d423b608f0b5d4763dcb58c0dd9e4673b7c64ecf64241947cf1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560a455baad8eacfe612b059e56e9c5ca08dec61a49e2ca1d556759a08beea`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 143.1 MB (143142590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bd3503415fa5eb2be4bb24bbf854e74951b39a17b36da6a34665776ee9ce`  
		Last Modified: Thu, 09 Oct 2025 22:19:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ec7566968ec0b38f9fcd664c0a76788d6355570ff6a025ef3c3814c9d4a5f4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19346350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09fc1092b2dacdfd90aa9e7fc9dc2a390728b7adb66b4b6d0d246c3a7d349f6`

```dockerfile
```

-	Layers:
	-	`sha256:ba1feeaa24aa0edb1e0207d146fbf98ed07cf1c172df7832f9f75b0a2ec01b20`  
		Last Modified: Fri, 10 Oct 2025 01:18:08 GMT  
		Size: 19.3 MB (19331560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d077e9693178dac3d582e39314dfbd2bb0b43132683826bd3a3ef92708f84731`  
		Last Modified: Fri, 10 Oct 2025 01:18:09 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:9a3ad210f7d02295b4d8ac56cec23c254ec53c1d0f620acbea649d15b3ec45b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:da420d243a5f5deec5501a795dcec056be107d4080bac2cc62680fe413736331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186062757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e95bb3ab43d416620b526087706fea37c9724a7ad23d2c39aaf36e61cfce2c2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081cac45e5fb7bc52c7bf496d2ccc3433f84dd8702adc9fa84d467cc2be5543`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb1361c757ec00d31a8c6c88058fd62b23da12af4290edf2d3b2c636f6da5a`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 6.7 MB (6746865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4540fb962b4d5de83708d3245134aac24f8adcb8d8457e317648dfe877db60`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 94.1 KB (94146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebe16a8832263871186c0dda7eaada9cdcfd4f1a4bcc90feccdb47acfff940`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 148.8 MB (148814487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda935e56c9a4a7f7f77e60fc31b89aa8dc68da689983df8cab450bf7bace1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:583945997ea59965ad3f4c7af3755f49f3658da3a092fb6c7fa0256b5cce262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19372017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde41f672c26b2756bcd8b10a33e18c6578776958d5d196d11efa808359a758d`

```dockerfile
```

-	Layers:
	-	`sha256:68c6611438f216e71285b4641824919748c76887cd70a29dc14cdb6c0499bea8`  
		Last Modified: Fri, 10 Oct 2025 01:17:51 GMT  
		Size: 19.4 MB (19357356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84946b9639aa950d309fda6bbfb20d1060f026e4f1e503028ec8f54814f3f48c`  
		Last Modified: Fri, 10 Oct 2025 01:17:52 GMT  
		Size: 14.7 KB (14661 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34933f25fb92bffb2a6fbf696e48dc327811da2099ac14a6873c9594b44aa9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179543247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaf1df2b73e2d423b608f0b5d4763dcb58c0dd9e4673b7c64ecf64241947cf1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560a455baad8eacfe612b059e56e9c5ca08dec61a49e2ca1d556759a08beea`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 143.1 MB (143142590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bd3503415fa5eb2be4bb24bbf854e74951b39a17b36da6a34665776ee9ce`  
		Last Modified: Thu, 09 Oct 2025 22:19:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ec7566968ec0b38f9fcd664c0a76788d6355570ff6a025ef3c3814c9d4a5f4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19346350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09fc1092b2dacdfd90aa9e7fc9dc2a390728b7adb66b4b6d0d246c3a7d349f6`

```dockerfile
```

-	Layers:
	-	`sha256:ba1feeaa24aa0edb1e0207d146fbf98ed07cf1c172df7832f9f75b0a2ec01b20`  
		Last Modified: Fri, 10 Oct 2025 01:18:08 GMT  
		Size: 19.3 MB (19331560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d077e9693178dac3d582e39314dfbd2bb0b43132683826bd3a3ef92708f84731`  
		Last Modified: Fri, 10 Oct 2025 01:18:09 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
