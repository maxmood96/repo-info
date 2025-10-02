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
