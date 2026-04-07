## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:f525a863a90c9bea6ec08e2b48fe8c68c22c5eca04253817e96866a956b9e9c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:6ade9cb543892dc2005c85fc1b4a74210da8cbc633ba29ea0e7a363486faa8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094996610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3883164fd22f97ba3567f3aca9b079ed2c261f9116fce02bb4cb38c402b291`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ab68a8765d2a0bb4fbd79e885d30475c96d517d9f388fd717df7df6a58cb6`  
		Last Modified: Tue, 07 Apr 2026 03:31:33 GMT  
		Size: 110.2 MB (110193398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61184d2a7dd89b65d8ea9c22edbcc83d7777c1852fb9503e9f765c0904cebabb`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 371.8 KB (371819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78675698bbbb43c8f40b4c835d17cb575878395b5d95384101aa6d449081b144`  
		Last Modified: Tue, 07 Apr 2026 03:31:30 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed39434b1f48964c8be41d16116e0f3d41c2cf9522aa1be7797100f8d83d55`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 27.8 MB (27840327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d771503b03b06f0248677850cab72eb9be0c6d88887cf877358d7401735bfe71`  
		Last Modified: Tue, 07 Apr 2026 05:02:33 GMT  
		Size: 784.2 MB (784242097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8f1a997fa44bc12440d608de9b9632e1f26040123ce46fd5a9ff948fcc198841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61807644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43ac78852ee853c63f0082a7dea027a57c1d10ae9e77effe1544a450396e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f598ca81494bfb9404de345610bb5028b947fb79b08928c4970aa0fefb718fd`  
		Last Modified: Tue, 07 Apr 2026 05:02:21 GMT  
		Size: 61.8 MB (61798283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3742ccaf8533ab5b1bf1cd0ca8c83ee95bbc8e7625c5386d8452e8d7309bf485`  
		Last Modified: Tue, 07 Apr 2026 05:02:18 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:daca987a1a2f76631abce62ce4be783354562949a8a97c4f4ef7b2563dc838ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 MB (997126498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c3341541c83a08ec2a6c930ae0df00e6b4d01ca97e8c7f458607f587abbfb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc58942ba23c0013ff4f043dc403940a128b600496526dd7a6c1ff107a363a28`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 105.6 MB (105606215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1a89472c625e25828173ec6e90ca03edabd608f21ec8d06eea1f387c4fc9`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 371.8 KB (371817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f32cbbfee1b751cf080817885147f380443df091a1789a6f76b47b867472e3`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e52d4e6ad307b275501259d4ff705bb40b6264b227536a5d46c28979dc6e86`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 26.9 MB (26929634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8668c2db6917b395bf1929e634c15c0002acf8e95b856ad02795bddb2905389e`  
		Last Modified: Tue, 07 Apr 2026 05:09:01 GMT  
		Size: 698.4 MB (698378347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:307ddec5f3bd8bb84a01c0734dc1f8465f934a3c922a401018a57acc8049b172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f880383f6626972e0645b88ee16804e21e6f7f22144cbb80cc60c75b53755fcd`

```dockerfile
```

-	Layers:
	-	`sha256:18241b55135ee1be315b190a49552380e0ff95862dc021c33c9f3f773fc3d8ff`  
		Last Modified: Tue, 07 Apr 2026 05:08:49 GMT  
		Size: 61.7 MB (61729001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9c6324a26829a8542921331ed09d41738ab6a83f08321f4154e5f8c500dadf`  
		Last Modified: Tue, 07 Apr 2026 05:08:47 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
