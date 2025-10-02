## `ros:humble-perception`

```console
$ docker pull ros@sha256:410892dcff1d92821372a4b59c0961ba99c0fb6458e239cbdf56c789d5e23747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:c5a0637f253069ce8a1b53d0344a91b3acb08ac353a51de9f31a150f96ac5f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.2 MB (955152660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72087975709a0fd197433652db2c305391c416b79b885d5ebc7bb4a6712db62f`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4205dd24072fa6c493e735b2530ed8c82d47cbce110866bfba44553e9c4ff6`  
		Last Modified: Tue, 02 Sep 2025 00:14:01 GMT  
		Size: 1.2 MB (1213974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2705f0adc4adce62066a1177a7e58cebab9068990c3a4ab2f7291a1c70afc11`  
		Last Modified: Tue, 02 Sep 2025 00:14:01 GMT  
		Size: 6.0 MB (5995240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba91d05e8ff7416d5bb177525057440404b9a1c4bdd77f7549d7f7da6f6c014`  
		Last Modified: Tue, 02 Sep 2025 00:14:01 GMT  
		Size: 97.2 KB (97173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e756fe699fedf8270691740b6f43d00359cec0bebe067e5b98c8872cbd8fd0e0`  
		Last Modified: Tue, 02 Sep 2025 00:14:13 GMT  
		Size: 104.6 MB (104590615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a886e9df23356de168fcfac31a587b1c0a6e9e6f85e9348f2f06959e818123`  
		Last Modified: Mon, 01 Sep 2025 23:41:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc64d1644dd39fbaef54bd357df3cd2994a83c3966e8ddbfa9ce93d29efd396f`  
		Last Modified: Tue, 02 Sep 2025 01:12:17 GMT  
		Size: 98.0 MB (97961529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2826d7d6374881ff52405011541ea3c8add702456f18f117d8018e9d99b6a591`  
		Last Modified: Tue, 02 Sep 2025 01:12:06 GMT  
		Size: 372.6 KB (372627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3eb779328477cb7de4b28b59895bf3e53e62b5dceb19923176a80b4332404d`  
		Last Modified: Tue, 02 Sep 2025 01:12:06 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a35c701e86cb204242548ef2f1881f664b9dc69340e6535ad374aa88634e29`  
		Last Modified: Tue, 02 Sep 2025 01:12:08 GMT  
		Size: 23.3 MB (23317329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bad7b104a0897f23a28ba250ee53b524f1ab8719c8db4ff6ba540b2dd8fa4c1`  
		Last Modified: Tue, 02 Sep 2025 06:57:08 GMT  
		Size: 692.1 MB (692064586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b5fe69aae2668df2c36e200096795de64c80289c63db30187c057df52fa51615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58775768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7351935c63f324887f2e0155b806d0dff404b28366d68f8d4ab606371fae1cdc`

```dockerfile
```

-	Layers:
	-	`sha256:61d4bc57e773b71575911b23e12eebaa8ddaa781bd9abf1648c7888935758061`  
		Last Modified: Tue, 02 Sep 2025 04:17:26 GMT  
		Size: 58.8 MB (58766373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb15653a1a2c40e8eb2e9caf563df1de681abf3d569cf44bcef82298450dc666`  
		Last Modified: Tue, 02 Sep 2025 04:17:28 GMT  
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
