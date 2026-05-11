## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:eca228a2dcdf0e8ce6db4501d14ffd53065bea71cd96778c53a02118931f0863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:674d62e1f97ba6ee307067805923bf8491dec22d01c38b73f4faeb9faf4b417b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263798674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7dd42b2c3e9b66ad0b0570416732258044ccc27299addab206174fe92a148b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:58:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:06 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:40 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 18:59:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 18:59:40 GMT
ENV ROS_DISTRO=humble
# Mon, 11 May 2026 18:59:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 18:59:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 18:59:40 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:46 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb80aca26f7323a4c05c7407144dbc29939fc8bed1f0eac2be917fe4a080f7fc`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 1.2 MB (1215560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b22082ad8b9356a2dc5b871f9d097cdc16dd83fa3b8a005117663efd30385d5`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 6.0 MB (5994781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e673deaab41171f1d0b885f91abb5c46c069411710bb9875fdff17a5894f9`  
		Last Modified: Mon, 11 May 2026 19:00:09 GMT  
		Size: 97.2 KB (97243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572089fd39981cf3239cc207928f7dacc413065e75c598d50dad560a792da1a7`  
		Last Modified: Mon, 11 May 2026 19:00:12 GMT  
		Size: 104.9 MB (104862679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9278dcb40092814e1a4fdcddd11168813114ed14329d356db0f1c08b80734442`  
		Last Modified: Mon, 11 May 2026 19:00:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e528cd91c005e9aef0cd99d0f250b3a608a1e71da815c0a4571ed040453bf1`  
		Last Modified: Mon, 11 May 2026 19:11:39 GMT  
		Size: 98.2 MB (98158637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ed9119ee2c821ffd02cde9cc2bb330a626630a5865487858713a6442738f4`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 395.4 KB (395364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a6637e86fa5fd08f8dbdcc1d52e9296862dbc2421c7f4831f4b3bfed03fca4`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9314fe91b6363bba4359d22db00281230e5d275d9b96dbe235bba8035b006405`  
		Last Modified: Mon, 11 May 2026 19:11:37 GMT  
		Size: 23.3 MB (23335210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e569e599084d222ae97fa654500009e022941c369e839968316a7d6d85903d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c1d51488655967b281148e9be57304438d5d3be7df0f093310967e3b19738e`

```dockerfile
```

-	Layers:
	-	`sha256:fd3addc3fbc113a1c32e37ba3c3488778753f0b86241d978029378d0c526338d`  
		Last Modified: Mon, 11 May 2026 19:11:37 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207f4864cfde1b671db333f6c722d7da9797d670e2844d241339ce0993a84041`  
		Last Modified: Mon, 11 May 2026 19:11:35 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:57d635025f6a38c670dfe110265969d3e76c3c76a63e19ed15a11dfd55878bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256408848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549c3db209a9be76e705d0bd1c4a67c9215886ea321d5cfce3da82822240aad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:58:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:18 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:58 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 18:59:58 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 18:59:58 GMT
ENV ROS_DISTRO=humble
# Mon, 11 May 2026 18:59:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 18:59:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 18:59:58 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:08:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:08:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:08:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21105286df146bcfee570e44f0c2084bab6a1650e301e96c71ea0c5b366164a`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 1.2 MB (1215746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c730a6a208f443fefd548a8f3ba5e9897dd637a97eaadc5ad1e721c5327bca`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 5.9 MB (5949231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5c8cf6d70219c353d71b074227d00fbcaff0cd2f7a0778f99b4fc6d0d6819`  
		Last Modified: Mon, 11 May 2026 19:00:24 GMT  
		Size: 97.4 KB (97376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bf0daff854886510375744ab2162a5f99a2a1084da4730c0e0fcf1fa7d49a0`  
		Last Modified: Mon, 11 May 2026 19:00:28 GMT  
		Size: 102.6 MB (102616871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5430748a99c3d3af061e4180d3bb3188e758fa68689641a55b690c235300f66f`  
		Last Modified: Mon, 11 May 2026 19:00:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7227d363f715b7e63b59ca1662c431bcdebe731eaf8083ea87e12b0521ff9746`  
		Last Modified: Mon, 11 May 2026 19:09:52 GMT  
		Size: 95.8 MB (95795943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d5c0fb8234bd343f07946df683ba16a9bbde83d8312a89d96a85f8978b86a`  
		Last Modified: Mon, 11 May 2026 19:09:49 GMT  
		Size: 395.4 KB (395360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4a447dc22863a13d2c639b383919494dcd30adccd1d5225e6fa7a04510dc1`  
		Last Modified: Mon, 11 May 2026 19:09:49 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7cbd63ef1f4425c347ebfd63e73256fb7a87e71792e0a50113b211b73a491f`  
		Last Modified: Mon, 11 May 2026 19:09:50 GMT  
		Size: 22.7 MB (22729047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:5e4309f3e99509c1a83c4687660c1fea282ebbbd4a807858f8feebd930f71e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d1c0d1aebca9b053a4d428f6d61b8508feb93bb4ef46f85abb25744d08fa09`

```dockerfile
```

-	Layers:
	-	`sha256:e1a5b7c78aa2d47c751a44fb10a887416754c3426bb41e67946242fca5f84663`  
		Last Modified: Mon, 11 May 2026 19:09:51 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a49eb17b5c33b22747041a6a78328b2765b6c0e25974a1020cb144129d5affe1`  
		Last Modified: Mon, 11 May 2026 19:09:48 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json
