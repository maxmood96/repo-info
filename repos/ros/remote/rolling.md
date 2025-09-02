## `ros:rolling`

```console
$ docker pull ros@sha256:25629e83353ea9fc23179f65a59f698e1bd06a4aa7ea0a34b4102bad9ba1ae95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:66de3f92af7e95fcfac129e90bc5cb1da1f421cb2c78612a3ee1542e9f325fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310400054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bde48799b4aaefce220d8b3d1fcf2284d96e88f04456c6b0594cacfda0c18`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a37d70e90a7d664105dea1987b320d87a2f03f888a701e8c119b5ff2f38763e`  
		Last Modified: Mon, 01 Sep 2025 23:41:21 GMT  
		Size: 683.9 KB (683852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683da3131eb22696ee1fafcb5f2eaf8378dc9d26956bce0f0444b6da44efebe4`  
		Last Modified: Tue, 02 Sep 2025 00:13:59 GMT  
		Size: 6.7 MB (6746730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd06cb60726529ab14c33cd0e549e60ff60afd5cbfb5e3c025eddb450bc7a8d1`  
		Last Modified: Mon, 01 Sep 2025 23:41:20 GMT  
		Size: 94.1 KB (94066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007cbb38796d10e52a782b6ca676f15631b28b4af68e7bd4feae2f16fa8b58c`  
		Last Modified: Tue, 02 Sep 2025 00:14:08 GMT  
		Size: 134.6 MB (134573911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a886e9df23356de168fcfac31a587b1c0a6e9e6f85e9348f2f06959e818123`  
		Last Modified: Mon, 01 Sep 2025 23:41:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890398f342aa88c778c4f5ec79b47e448e4be344d76bfe12abcb5525c8dceb2a`  
		Last Modified: Tue, 02 Sep 2025 01:12:19 GMT  
		Size: 110.2 MB (110184026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a000dae7914aa2f9240b525d7ace99c6aeb786ed92d156beaa2e7db638db61`  
		Last Modified: Tue, 02 Sep 2025 00:49:53 GMT  
		Size: 353.1 KB (353120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d54fcea91659938ec9ac4eaba7bed60e4ea22031e9869f9441a2d988b9f167e`  
		Last Modified: Tue, 02 Sep 2025 00:49:52 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4f25e282b9e272bff5eb5fad06859e7ea0a1568ef3b4e8a7a21007e3055071`  
		Last Modified: Tue, 02 Sep 2025 01:12:12 GMT  
		Size: 28.0 MB (28038618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:bdde48fcba1de559a19420e232f9ac7c10fc1a5cea882cb0653a1645d6713166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24534893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b590eceb7c41e911fe0f29f1a731bc736b661d53fc1a696a3d0c49ea4cdf7b3`

```dockerfile
```

-	Layers:
	-	`sha256:dee4d445b04a216b5463f19c9304f051dad012ed4cc9112430267cf11384e360`  
		Last Modified: Tue, 02 Sep 2025 04:18:13 GMT  
		Size: 24.5 MB (24518486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed8d5fbfeddf67ce010f205687d8c782ca6198a96fd8ebbdee3c280d7cd4c1`  
		Last Modified: Tue, 02 Sep 2025 04:18:14 GMT  
		Size: 16.4 KB (16407 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:91f49d3943b8f5a73e4adfd58870afec88276191f1fd49a7a8289f3ca297b53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298754440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d3fe33da31f1eaaa4d7ce0ff071020a9efa6fe67a48d91a2d1628f51dd25f7`
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
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
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
	-	`sha256:d194f3a8bc2607370aa62995f0b184b133e317282e29af806497ef043c0a13d6`  
		Last Modified: Wed, 13 Aug 2025 03:32:57 GMT  
		Size: 129.3 MB (129288135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5e11a61da7887a347f196979a7b818f7d26d60ce957fe1491c32525fb607df`  
		Last Modified: Tue, 12 Aug 2025 21:10:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b174b07e4fd82c1ed915d1c09be6c2e0d68b3f2e56f8086bd40cfe7db6e8ddf`  
		Last Modified: Wed, 13 Aug 2025 00:15:10 GMT  
		Size: 105.6 MB (105593476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edd2563a26e5f677ea8ee2fe2f5e4b7f6045083eeae9823b9f9896cb6cc3cb7`  
		Last Modified: Wed, 13 Aug 2025 00:15:00 GMT  
		Size: 352.4 KB (352436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e8d5b7bd6c7ce007dabd35e360e1bacf2df3ca6857316041805234527a9ccd`  
		Last Modified: Wed, 13 Aug 2025 00:15:00 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5edbfa648ef62a2c40305c41c70cdedb50659862a1b93e3511ad89b05c40178`  
		Last Modified: Wed, 13 Aug 2025 00:15:02 GMT  
		Size: 27.1 MB (27119279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:a2585c6511f51d96a5fe4dd299debb4972d3be2453c7ff2752c7925317b632e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24557290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210cf8245fa15173b6d3084aae69c614201f7cef1cd8aa7e665562f9d2e02f0a`

```dockerfile
```

-	Layers:
	-	`sha256:abb4543798ad3d97c4b6bd70260846d1b39cffbb476d86d812056655d6a57f0f`  
		Last Modified: Wed, 13 Aug 2025 01:18:08 GMT  
		Size: 24.5 MB (24540746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d7b6e2b0b0aa4d2b28c2e944ca2e02df71f59281eef2f49271dd55844ffc37`  
		Last Modified: Wed, 13 Aug 2025 01:18:09 GMT  
		Size: 16.5 KB (16544 bytes)  
		MIME: application/vnd.in-toto+json
