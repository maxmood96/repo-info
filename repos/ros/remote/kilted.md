## `ros:kilted`

```console
$ docker pull ros@sha256:e6e9fa5599884785b09df352e47ac25c09a3ee926d876e6697e868b60cad83b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:245dec30373a422fb1d92173ebe9b71fc49b812a18203f0831316c5872eabc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310832015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f804d63011dc6ad9dd51273bcebe4746323df681ce5790afd38e8a3e7a3413c`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:7d1dce87a7f4acd9c8a37db6070c5901c6b8b29cfcc2e7bde7ff0808cddffd70`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 110.2 MB (110185948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30531d5abaa989826e78461584cd1956e1f59a63a17a0494374eb70a69ce2229`  
		Last Modified: Thu, 09 Oct 2025 22:21:08 GMT  
		Size: 362.7 KB (362682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30687b244cc914ab1a8ae574c29b80cfb7d1c51ffbf978065c7872711fe0512`  
		Last Modified: Thu, 09 Oct 2025 22:21:08 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292b4fa4c8d3eb0f4f13b4294e62df33588750da9560b319522a4e08a4060761`  
		Last Modified: Thu, 09 Oct 2025 22:21:10 GMT  
		Size: 28.1 MB (28051019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:e0be485607ce3ede8292901fcbceb96e402a306028a150c7bb0d5eb8b4656996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2ecf2b3bce88cccc16ec1876b3508cb10158c385156567945b3b5780cc4aa8`

```dockerfile
```

-	Layers:
	-	`sha256:77e1530895f1a77f271efe450d4f37a1aad157be3b3812723ef389743ebf7ef0`  
		Last Modified: Fri, 10 Oct 2025 04:17:52 GMT  
		Size: 24.7 MB (24650296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cae5dbfdd139e5b8fae557cf63a232ad8346ac7b6d8ff692831f1808e8fb9eb`  
		Last Modified: Fri, 10 Oct 2025 04:17:53 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:29385e97ddf1ce7f40f8317554043209cf1c7f32d0a90cc902fa828c34262af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299201038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9563985258e13f52ce7273effaff1fdd693e7ef26cb015f1e8bbeb4392efd6`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:e54999cd408b26d5a3591d807fe057f8f0496922b72c4ae057adb587b840f699`  
		Last Modified: Thu, 09 Oct 2025 22:21:32 GMT  
		Size: 105.6 MB (105594196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1813b12f5e0a79795a4d2d720c543dde8ed912e3a4265f5b9fa49285e11a6362`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 362.7 KB (362687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b681a1245bedf2115e5b1ae357a6ae27fc654b24b46971ec2d199a75baa48ca5`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437755691707c3c0f86472a9d675632fbcef51af972b17e23294315534f28aa6`  
		Last Modified: Thu, 09 Oct 2025 22:21:28 GMT  
		Size: 27.1 MB (27137484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:f609b3a13a4a6c8d03a0094e8c27bedbca4f2066b03e3605a1d09b97e9bf8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f304a3bef5e02f27451960e601a0202fd6bdaa47512fb2c71984545db5730d6`

```dockerfile
```

-	Layers:
	-	`sha256:fa81087d263d8fe91c7bdfe2d767a99c5f0e97e63a56a03f8606c5f22ba86637`  
		Last Modified: Fri, 10 Oct 2025 04:18:11 GMT  
		Size: 24.7 MB (24672557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0543b08ca8cc2d954242fef684fa9113c6996bbd791171b4037fa2eeaa5c6c4`  
		Last Modified: Fri, 10 Oct 2025 04:18:12 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json
