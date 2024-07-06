## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:8d520229fe10d1ede5498e0572f2224d076d27499c26439be3fe541fcb966154
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e77cd91fdc7fae1b2cd77edb64e4eb624127ce2ac51e41657b11cba2bc1978ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.5 MB (953546148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65106020985b7bbbcc612d9b0d9f19c3811ff05218b1dc4d0c3c388e8c39a3d8`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1edf04025a122811e708ccc8040d53a46e573f84b68d5247d9588ac36b74b7`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 1.2 MB (1214732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a9afb6d76657fc94397c228fd19083463ec0fe70881d152e5ba5b040054d4`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 3.6 MB (3624561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85780c0ead4f3a7f56e455d70f23d79210a63e1ba6103e67128cb281318b83`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34432dd821bdfd3e40b782714a265caf961044dbff025c9fc02e176f4bd90f`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab814f3f3a32d87ca5c6bde7c77d2578379a6cc59be2c305126c1aae06b0591`  
		Last Modified: Fri, 05 Jul 2024 19:57:18 GMT  
		Size: 106.5 MB (106532664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88c71908435c810f2f816f9b482653ca9899fb8aa44f1478df5aba224ab6e27`  
		Last Modified: Fri, 05 Jul 2024 19:57:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0a8f3ddd40e3b7949628886d4fb748c67e0f153af4715939b9fd03c4daa83a`  
		Last Modified: Fri, 05 Jul 2024 20:53:04 GMT  
		Size: 97.9 MB (97935789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eed1499953b6d648ae2b5c628b115677ca0fc742b4744fb77302d01efeddd7`  
		Last Modified: Fri, 05 Jul 2024 20:53:01 GMT  
		Size: 329.6 KB (329596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c691b5132d1afea9805b2b7771be511fe3e6bf7b87d09baa38df44de22f974`  
		Last Modified: Fri, 05 Jul 2024 20:53:01 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affb762110c9fb544c0aac08b6265854a76a1ac0193677581988530512dfb814`  
		Last Modified: Fri, 05 Jul 2024 20:53:02 GMT  
		Size: 22.8 MB (22812624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566925a0bc3e6e06f2b5e61981fd3105d0f18ffcf5000e6d5aa4cb38913159e`  
		Last Modified: Fri, 05 Jul 2024 23:00:27 GMT  
		Size: 691.6 MB (691557199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:435d09fe0bd1ef768ae503ac6c05ba4e45920fc666e0813a0a0dd783f71ee428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57024659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b003bc08cdf72dd793b9fc9bf1637436aa8fbdd9ae44b0bdbb9fcf93e1bb37c`

```dockerfile
```

-	Layers:
	-	`sha256:59a74860e5c129177e3f0543075f4ac8e5c8702d0c15e368103c6c8996dfaa0a`  
		Last Modified: Fri, 05 Jul 2024 23:00:17 GMT  
		Size: 57.0 MB (57014993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:866741681bc73200af099900de1e3dced2401029a96591b7f7bcc04c4f2003cb`  
		Last Modified: Fri, 05 Jul 2024 23:00:15 GMT  
		Size: 9.7 KB (9666 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d2b16e44d76dbcb854fcc0b99f82061537ff92b8eb93bf71fd5400b8449eee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.9 MB (913939947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248d9599dabe2e57eb67b4014aa2fd69ef92228e1dbfe29ebc477cea29125b06`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c38d1cafe9b3c575c695d60acfdcfb8a3d93189dcd0392ab6700170adba3c1`  
		Last Modified: Fri, 05 Jul 2024 23:35:48 GMT  
		Size: 659.5 MB (659452856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:752677fec29adc76b5168a3947fabd7e403bc1042cfaecb15654b5e0c0c57d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57022234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f419999d559b605477a8437ce23da55ee013564e73d801042186ad50b7fb4be7`

```dockerfile
```

-	Layers:
	-	`sha256:54c93fb447016e5e9808edc714c2786b411bd71f1f0e3f9668473b6f34a8bc7f`  
		Last Modified: Fri, 05 Jul 2024 23:35:36 GMT  
		Size: 57.0 MB (57012206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb544d2b97e6908ddc50f7c65823dd823d17544414c8447aa649843c04b7f13`  
		Last Modified: Fri, 05 Jul 2024 23:35:35 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json
