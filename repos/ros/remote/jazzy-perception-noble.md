## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:5b201c72fd65364578eec929c3ba46f4100bcc0e2d7682bb8bf4ac1a282a9fd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:35a50d52f1900f0bd82ec2ff4ef5ab745a379bd121d24bf78ce2005509d78b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081122464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9a41f1bdfc14d3f8e2a25f14469d8a3581ba0251ac4df207332e4fc4174595`
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
# Tue, 02 Jun 2026 10:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:196a879123d1a0ba3b4bc9bc5927e8f1082c1469548d76d7d4d34a60f9838916`  
		Last Modified: Tue, 02 Jun 2026 10:18:35 GMT  
		Size: 785.1 MB (785102331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:03476dc4b14145d50d5dc9f14cd084207b27214da7ae40f7d0d196f609f0807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc9082a760a3c5ac61e21cd2a16decf68e7b0557f088fc17b4c46b8db580a9`

```dockerfile
```

-	Layers:
	-	`sha256:c0dcdea6dafb2c7b0090103ba99845a6be3ef110178a82b22326439a85fec1ce`  
		Last Modified: Tue, 02 Jun 2026 10:18:22 GMT  
		Size: 61.0 MB (60966307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47c67b064ae76fe3190154a8e0e43f35ae8edd71c882d26292b8c31d6f67699`  
		Last Modified: Tue, 02 Jun 2026 10:18:19 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a63f1b99d65f61d357f2c90517ee19cb8ac20deffb150fc7411c1803e1dd3c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.7 MB (983709754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b9d737ffdc7dec611fe7b91ffeebaad4771d1bc1c73386002b17add86f8e16`
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
# Tue, 02 Jun 2026 10:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cfd7060f734905a126f9fa98954fe08e6f72cf300329b60024553ff7da0c5aba`  
		Last Modified: Tue, 02 Jun 2026 10:17:17 GMT  
		Size: 699.2 MB (699231719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:170302efc4c417ebe80fa810687bf3556ca493539d37c53561c52b84370697f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60906245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e4455f4155508602b2f18cf4aaec4d8b55a30aaed567c34eadfffda1bafdb`

```dockerfile
```

-	Layers:
	-	`sha256:4f01fe505ecf28fa29ced4382ca8a0805a1e8ad5575f1b94e6b17537a3e2eb4d`  
		Last Modified: Tue, 02 Jun 2026 10:17:06 GMT  
		Size: 60.9 MB (60896826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c174c53dca8fd304686d094eca4ca49afced1c47621f0ad004ebb5e13f4cb68a`  
		Last Modified: Tue, 02 Jun 2026 10:17:03 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
