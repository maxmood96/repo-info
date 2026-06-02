## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:6513503d0b10e919fbe8134981d4f9d19b5c1f9b045b87a9fe3b0b9e03e7c2a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d7452f46711eaddadeb4a19e81a3e38fa2bf95ff792059f849efa5e94e2e891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296020133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ff726b8762c4fad9f9743ac1f83da1f1f939087042b5b93fe97a7c0a17f2f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae782a0a6284fab5ceff612525d03c2fbafd66097e0159150b22eaacf34ad2e`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e16aa32a6f9534a9122737424f7b375a0eaff7786e7cf7ba9a29db00fcfd0c`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 420.6 KB (420586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d37a7b1357585f8769a5f8d1cf601e8e467f7c0572992d06579b525d49786`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135cc175fe2c44a1520fd201bec2fa8a7ca4e4d45a82979677abb1c9e9759159`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 28.1 MB (28068985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d9e9b81219f2c665bf289ff8b6f64e41fce793f5fe9afd0e31360bdca40a6051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24806888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3389965fc524ceb14afd9c22f9adf105f8675e46fbac5719f8c67edecba3392`

```dockerfile
```

-	Layers:
	-	`sha256:297c78211e937682121d3fa452f5feab0b42dfa1e45ced5bf7d2d0958bf931e6`  
		Last Modified: Tue, 02 Jun 2026 09:15:50 GMT  
		Size: 24.8 MB (24790559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93415d3bec983b8e517f916b69bab409c59dd98f7125022f501eb653114a91a8`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e0e0a8d3dfc4bd619285fdcc995fa184db470358b39908b9b7a1e2fd470750d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284478035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beda46c225fb76e59d2691134515789368beaa34305f07a4656f83b2e12964b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf587848da08365dc078d9f8848d4c700e5caaba2d9e1b99f5c194ec9efcb6`  
		Last Modified: Tue, 02 Jun 2026 09:24:05 GMT  
		Size: 105.6 MB (105607043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e960a7cf717d5318e8988413707746a9b3250dc72a5dd6d7b9bdc74243bf23`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 420.6 KB (420584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb59913b64666476335b92fd5df610e1cdc74d963f4f226bc9da7f41650a1e9`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c2eb0a2c9085ea587ef92b45b43934fa4b247e6b9c3417551e87c1cd82a`  
		Last Modified: Tue, 02 Jun 2026 09:24:04 GMT  
		Size: 27.2 MB (27177935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5191243aa94ad5530671e9b47f58859857938d1290adccc35ac5288fa54c7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d90490eea068b87e1b19be14a846532ac88814c0ef12c6c6851ef4e3c0f52eb`

```dockerfile
```

-	Layers:
	-	`sha256:9bdcb5d514af7eb89ca037fcae0bf6117d170187e24fb192264d1f4e242a69ba`  
		Last Modified: Tue, 02 Jun 2026 09:24:03 GMT  
		Size: 24.8 MB (24812814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6923054ddc4bc7764756b1aafd6ddecd708152732604523e66727a0133457e01`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 16.5 KB (16466 bytes)  
		MIME: application/vnd.in-toto+json
