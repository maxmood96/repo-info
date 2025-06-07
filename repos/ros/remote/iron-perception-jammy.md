## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:a3a06835e0fc04171ffbed2307a5571e52c41c95987dc68b5237a5c188c6a8d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:abecde4d2da59d71741c97f381c4123cea5ed425192bcd91dba6a2b4b44ae279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.3 MB (960272361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c597b31155bc87299d34ed59833847b7d36d0ee2505c79f6f1157d483104c8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb9b3cb725d901af48e802f77ce73047c3689a12baf83905c56bd207982caf5`  
		Last Modified: Fri, 06 Jun 2025 22:49:19 GMT  
		Size: 1.2 MB (1214032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f141b6dc13f270c4f52ae21bfdb4af90e188ce8b57cd7ca5cbcb4308ea5180d5`  
		Last Modified: Fri, 06 Jun 2025 22:49:19 GMT  
		Size: 3.6 MB (3625827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7471adfa037bc44bef892286aab80c5af5331c2dee7b03f68c41a2b7dd95517c`  
		Last Modified: Fri, 06 Jun 2025 22:49:19 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a016a720aca2677cd85c28ae7e62ff9f9cb4864e2917d84c89ecfafd14c65b4`  
		Last Modified: Fri, 06 Jun 2025 22:49:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f14b329843fd765c3130965a174e03696f308b064db2c5aed6b4e45bd1aa2`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 124.4 MB (124356749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026118e86113f0f5c37c1d19ef1dd9ef5197c1ef2c62dc7dd8baf86a497be232`  
		Last Modified: Fri, 06 Jun 2025 22:49:20 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b53d37ed5500a235844cce8c59eef26c09e6c6d3fcdbf06e9a4deda8b98fb3e`  
		Last Modified: Fri, 06 Jun 2025 23:09:14 GMT  
		Size: 85.0 MB (84979032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35e67328b168297627618c8d3ea48cafa10b062280414d60c951ef8280105b9`  
		Last Modified: Fri, 06 Jun 2025 23:09:10 GMT  
		Size: 330.2 KB (330190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facab70c82f5bcc5c39f5cd43289497ad735cbb1b4f6860429582c18b1c400ca`  
		Last Modified: Fri, 06 Jun 2025 23:26:13 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76283d507f7ec386e1442325e4c1328ea3f840e88a09e92e4bbeeed21c3d9639`  
		Last Modified: Sat, 07 Jun 2025 00:07:54 GMT  
		Size: 23.7 MB (23735265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bda2abedb143efe345b7c1bb7d6b69f326352dd46aa347e5dc1660459df4ac`  
		Last Modified: Sat, 07 Jun 2025 00:12:13 GMT  
		Size: 692.5 MB (692491287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e2a9eb751658e8b69cd254fb6e1040e71886f2c4edbb12b6802bfbf8367fc57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59443422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f97f15c92182655e13cfa0efabc9465177bcc532c55630e96932ee547cfe415`

```dockerfile
```

-	Layers:
	-	`sha256:ab306db0eab49a8eaeaf3d5752cc52138bb84bc1703a2550c97b158db59f821c`  
		Last Modified: Sat, 07 Jun 2025 01:20:46 GMT  
		Size: 59.4 MB (59433748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0426d5a3f1093fc4236ac4c719735072e3e678568cdd46bbc8b81eff4698770a`  
		Last Modified: Sat, 07 Jun 2025 01:20:48 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7b476c7d231ab22f98ba0b94cd76d5073fca933c1ef7e7d4eadfd7f61b84b6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.4 MB (920414563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cfa700a2bc2327ea55214e2f8191ac6202b9fd9bf82196d9352e0d4b93a652`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2146e7031324610fc8bbf7b474883917c4f0743612759dced572c0b451ba3f9`  
		Last Modified: Thu, 08 May 2025 17:16:29 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dcc592a7eac1b630f5090e3f04ebdba1f3a7e3c8efee89e7b88091bc398b56`  
		Last Modified: Thu, 08 May 2025 17:16:28 GMT  
		Size: 3.6 MB (3596933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e493107531d32f95fac752d02f6d303c00762d4a6ff8d710cedc2757cdc6c982`  
		Last Modified: Thu, 08 May 2025 21:30:29 GMT  
		Size: 3.6 KB (3639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922aafdfc15ae9c881fd82e4e3e53df73441681199b1b01db75310e5f0a45d84`  
		Last Modified: Thu, 08 May 2025 21:30:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9cf91867e168e459c65056e05887e6908749dc4d5082fa5add97df0dcc3561`  
		Last Modified: Thu, 08 May 2025 21:30:39 GMT  
		Size: 121.8 MB (121800501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18131159dd922a7314f395fa4055495df138d067d9b0194a8e9e18c53d2460`  
		Last Modified: Thu, 08 May 2025 21:30:29 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8bb4d88ffdb04c7bb60bd4f9a7691584cf0238fe86687876779447f97afb0`  
		Last Modified: Thu, 08 May 2025 21:30:36 GMT  
		Size: 82.7 MB (82653297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b752753349c66cc54bae91b0ff6c2817b0aa4356ef1b1f12a85b9dc8cf2095a`  
		Last Modified: Thu, 08 May 2025 21:30:30 GMT  
		Size: 328.7 KB (328663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7481703a07ed4e39999fd6961311bf8feaced94bff18d8a3f0c0a353b82ae545`  
		Last Modified: Thu, 08 May 2025 21:30:31 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4b919ac4e10b19850681d4db27a6c63e99919af01e71fe69023235b934c4c`  
		Last Modified: Thu, 08 May 2025 21:30:35 GMT  
		Size: 23.1 MB (23127145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c16731588425cc57c7851dbb0c7ef531dcde99f6a79e739bf0e19ccbaa9925a`  
		Last Modified: Sat, 17 May 2025 09:48:16 GMT  
		Size: 660.3 MB (660333265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:b5913426df1bfe7f686b3717ddbd49837b04be31a7c8a1d1f304b53fe0c3981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58340254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d4a35483e3ea0cb57ed9481ccc8f8b9a84a6c771aa7c7305b3ffc9b02c6b84`

```dockerfile
```

-	Layers:
	-	`sha256:4bfaf02f94ea0389156fd0ef34930a23bf0a31ea53dff10c6725cf966730506e`  
		Last Modified: Sat, 07 Jun 2025 01:22:09 GMT  
		Size: 58.3 MB (58330499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a0339076521f958a974a56004bb39eced99544a2e1ff39829df709ec4d70a4`  
		Last Modified: Sat, 07 Jun 2025 01:22:10 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json
