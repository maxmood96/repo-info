## `ros:humble`

```console
$ docker pull ros@sha256:00efc6996a8857489388da978ba6f9fc4322c7909f9b2a31d3b9664d1efa30e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:346ad7ade579a5ccf7839d9205ecbc5b34124b1ba0f8751f8c079cf17389eba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262607851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44566ffd4078a86cd9f17197c554221611147cb6ccd288faea8cc921fe9fdf16`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc0cb75a96fc365033e9c90cb0697634a996ee830f32708e403456ed01f4d52`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 1.2 MB (1214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b4e896071636d3437de6efb01a5545c16484eb75b086d3d310b105c98a95`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 3.6 MB (3625685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3e7277c8168821d69668561f0684a23df95676641b2f5bd5939191de98b0dd`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172492cea75e76031d73eebab577b7807873b0ab5dd42540f0472724085f12fc`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c0dd50fef2133f73e56fb7b321bd941e63e5126799a68a6c46d7639ae32857`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 106.6 MB (106624981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c48063d83a7c29eb89d52e692df6949bd3682caf3db40bec20778eff8176e`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e893907ceaa195a693dedfd545a53935733a67350077cc004aa4f25023430fb2`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 98.0 MB (97953904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021f2e34f666bc8664cff4806c8662a806201edef9ff624154ba152b0ada1c5`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137b6ba43f0df1ad8e21f42cb7c57d4412b897e0c6d7b5fdd3e9a4dcfc42075`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed447533d41473355fd6a2e0e7ae69b04a36d09b4960da437d919c2de5ae2cb`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 23.3 MB (23292617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:8c94b2b9f8c5c04ffdc5248aef8b9428fa1947f8f3229ff06e82a09be07fa574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22946485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de601485a4645a50399690478f834d7d94a954e74e181e0bbc22c107c8d209af`

```dockerfile
```

-	Layers:
	-	`sha256:c971d0b764205cf3140fdc4abc9003b8468c3f0453e47e5f125716d7df99878a`  
		Last Modified: Mon, 05 May 2025 17:05:12 GMT  
		Size: 22.9 MB (22929329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b3318e74973df3b3972da2026128cb7e4a5069307c99b1eda70aeaa980853e0`  
		Last Modified: Mon, 05 May 2025 17:05:11 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f9a1457dcdccc4770323824733de13df9136d1ef661c4069aae3e9339cd6168e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255048775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2e1288c1a5731884cddbd0c01810bd5c541856c7a64c1b6f8c2b3fd7d780f`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
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
	-	`sha256:cb9a0294d009c4eec5e2391695508957ffd90e81b450a700f767c52901c08ad9`  
		Last Modified: Thu, 08 May 2025 17:16:28 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd089382020f22def49e855c20fac44da7eaab36afaa0b76401347b835355984`  
		Last Modified: Thu, 08 May 2025 17:16:29 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf397c31a610cf57b769f67d08246772afbc66e9f315fe040521f76cac6d0c6`  
		Last Modified: Thu, 08 May 2025 17:17:20 GMT  
		Size: 104.3 MB (104332265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71f77027436cf6bba595cb99831adbc751cb050909152fe688b4d5925e9d8a`  
		Last Modified: Thu, 08 May 2025 17:16:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971dd4b19b510a2f1a71bafbc53170c446bf06ed71ebef714bbb5a905ad5e3f`  
		Last Modified: Thu, 08 May 2025 17:16:39 GMT  
		Size: 95.5 MB (95505714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f3d829f2919e9b050501cd51e467f893aaf8f0aa9bf6b034386ca901643245`  
		Last Modified: Thu, 08 May 2025 17:16:25 GMT  
		Size: 360.2 KB (360163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f517a73c8451d9a0acd02357f5bae55b878e2af322a55c7605fd57b82b898913`  
		Last Modified: Thu, 08 May 2025 17:16:26 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840fdee41f175024f1c811c9ab1438f29f706a096bff80e6a1db1540ab3bc87e`  
		Last Modified: Thu, 08 May 2025 17:16:27 GMT  
		Size: 22.7 MB (22680578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:735d365faf3e2a005af131b29ed7c84fb194ab14e67fd457ca0f21b2bac97c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22959638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1342f24acb5f21ff6a040847c0fc60fa02d5c1b13d9b7e6a9098949a9ca9ea6a`

```dockerfile
```

-	Layers:
	-	`sha256:d166feabedd0c6c522bc5a66b688d613f6017a7a5bbddbd5fc603ac16817f040`  
		Last Modified: Mon, 05 May 2025 22:46:42 GMT  
		Size: 22.9 MB (22942345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd35bda05b8da514e04cba0e28f92f24fff1f43aa001fd7e871e4d47b431802`  
		Last Modified: Mon, 05 May 2025 22:46:41 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json
