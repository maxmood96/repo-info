## `ros:humble`

```console
$ docker pull ros@sha256:3a3534452e220255701ed0ec557dd5f8eb6d085aa4a1ab9d41460a83a975249b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:bdd41deeffc019bf7fe4efc34fac871507f8ece09a0bd65ec9640366cfb63991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263088074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a14dfbe0bff884f6f5c29c4255ee87409cad592c0397a0b99630893966f00e`
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

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:087c6e3ed9a5424cf9ba35cca93a65578bb15fcb1edd72a79d72b841e9fc59fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23691240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ce1632ea3661b5daaf21e4377fc38aa03a9f74a44efe09325cc7c1e231a8bb`

```dockerfile
```

-	Layers:
	-	`sha256:58e5e07e60d9a972223c3c85599de585cf64622221dde90471cd6519a9163c00`  
		Last Modified: Tue, 02 Sep 2025 04:17:21 GMT  
		Size: 23.7 MB (23674849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b6c77e04129f9dfb6cdf69330a60a7e7ee887dd32885d810458a556b243350`  
		Last Modified: Tue, 02 Sep 2025 04:17:23 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2080f71d3725ed4dc54fc1f20ed6097870820a51defb2a45d7f6890978aa3961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255547141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac6c3982cf7ac8d76f82158ce6b5a9373ce1dc49d8d803ab3dfae33e0e487f8`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a77e6975807c8e890a2cf044fcb6f35d2ad716356d22e686083e5a2eeb97b8`  
		Last Modified: Tue, 02 Sep 2025 03:30:20 GMT  
		Size: 1.2 MB (1214284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f546c8afef9f167f7920525132e3a393c5e265d0a9a6593debbac17c28e538`  
		Last Modified: Tue, 02 Sep 2025 03:53:34 GMT  
		Size: 5.9 MB (5939801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67cddd8774262bd1585cea4cafaf2483d45c9ccf40fd9b97e2ae25383c8391`  
		Last Modified: Tue, 02 Sep 2025 03:30:20 GMT  
		Size: 97.3 KB (97334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309603855563f03d263dc74831526b419d8fe8202bbcd151947bb79427aec0d6`  
		Last Modified: Tue, 02 Sep 2025 04:18:29 GMT  
		Size: 102.3 MB (102315179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7181012bdacb622dc4363a2d97e413500bc79abc468fdb0865338aef72db48d2`  
		Last Modified: Tue, 02 Sep 2025 03:30:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3830518a807227844510586a5f280701a9e342ca9448b6ba1e9d42c126f13511`  
		Last Modified: Tue, 02 Sep 2025 05:36:06 GMT  
		Size: 95.5 MB (95537377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2639968e5a880d758d668f1bdb2232298bcfd893a8e7e206a44ca6860f89dc9a`  
		Last Modified: Tue, 02 Sep 2025 05:35:54 GMT  
		Size: 372.6 KB (372628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9500c18756a6f8de9a1166790dde2ca966657f538282ed04ee8e014fa69f0ed3`  
		Last Modified: Tue, 02 Sep 2025 05:35:55 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce374e2e7da7315854602ea26b084239e59bdd2ffdf97085f6b9f8248ee7cd8d`  
		Last Modified: Tue, 02 Sep 2025 05:35:57 GMT  
		Size: 22.7 MB (22706434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:f23a494c7cc99f680233bb6d2c01bc75f45869388a5df42787e429bf6cefb9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23704392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b82fa4adb74680dea65f5f3097be82a7194d7f23c7e11da9b98382d7710b57`

```dockerfile
```

-	Layers:
	-	`sha256:28bf1c457e08e49bec272783df5da8ef2731c2268e674fa40cc3c2d628dd6a46`  
		Last Modified: Tue, 02 Sep 2025 07:17:34 GMT  
		Size: 23.7 MB (23687866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe61c432abae06cdc69b95de75847fb01239917eb3eb41f7057a6f76ba1d76c8`  
		Last Modified: Tue, 02 Sep 2025 07:17:35 GMT  
		Size: 16.5 KB (16526 bytes)  
		MIME: application/vnd.in-toto+json
