## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:cea9c0d5a4394d6521447c893417ba5faade92f190ab177bf2870e368352e196
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:7c0b5f29d1a916cee2b43c5adf54c808fd9add5cafff50a77e5e9a7e46e2edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081629189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6376b15840456614296141b5a1c92efde60d93072b6b7b155c8ca951d75bd63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a248f2bd79ae227592752d26140bca43f6cd49805b445fabbd2379415a637d0`  
		Last Modified: Tue, 17 Feb 2026 21:55:24 GMT  
		Size: 784.3 MB (784302369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b754b1e403224a2b35a7e3c8092c75f0bacbfb3956697ccc7f3dca68e84444a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60737081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5617ec2c84a591ed8996711042bb670034e20a08c034c9911b7e9b1365aaa1e2`

```dockerfile
```

-	Layers:
	-	`sha256:04f544610ceaf65160fff3518c4466d4dd6c04726db246918fb926a07d22a1af`  
		Last Modified: Tue, 17 Feb 2026 21:55:11 GMT  
		Size: 60.7 MB (60727742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151fa5cb26c3959ecf68e7943343b2407b0561c5b29eebe45151103e99c9f8cf`  
		Last Modified: Tue, 17 Feb 2026 21:55:09 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8b6c0d1a597df8c8010c35b197e6c013bd28ee56772a9c6e2bfc5196e53565aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984165917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458d4d9e3e544078fa2555551fbdd2755eaa276fe77d151dae147867c4ceb96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632a26418f08c9068f128ad80934b0ec0503a1623ab7ab56e34428a5f7c2c703`  
		Last Modified: Tue, 17 Feb 2026 21:56:01 GMT  
		Size: 698.5 MB (698454503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5d115d51e9f2b2a7556dbdc3d028dc52a9627018450a708cfea2277583aac5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60667669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095fc92103fd36beb37abe141ed896124c1f77dece2a9a2735f2a4a095f59bb3`

```dockerfile
```

-	Layers:
	-	`sha256:f5d8ff15b2600356abe956dcd5df0f098cfe69cfc904538939e6f69b4f1fd843`  
		Last Modified: Tue, 17 Feb 2026 21:55:40 GMT  
		Size: 60.7 MB (60658250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cdb7267854d0b2a71fcc8c327810ceececd93dcbab1078c0b636ced02d6789d`  
		Last Modified: Tue, 17 Feb 2026 21:55:37 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
