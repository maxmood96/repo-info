## `ros:latest`

```console
$ docker pull ros@sha256:86808dfea395039494b4ce75d666c10264c353435b19fa8aecf74014a4500dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:3f3434e8c66b35b4362d43b3c68d4debb705121fc5f16e850b6174f3c304be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297737941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b861d78ba166e07b81f0322c6e47e9a5a15c07400fb36c636a290ede57179`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:bf3566f1f09c8118d736c936f8d9a1441accd489d516c4c0cc4ce205565840e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54591db849ffc7e9320f0f8b07f6aff008c44e2800052d8b4421c0fb50eca387`

```dockerfile
```

-	Layers:
	-	`sha256:4b44b6d9082678531c67b5b4669eb393bb2bde2e284208bf385d1745b965f939`  
		Last Modified: Tue, 17 Mar 2026 03:22:31 GMT  
		Size: 24.6 MB (24571546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ee0f1caabf1f9ddb69204af7f718f229e0be39a1a7af06bc7ed3ca02613880`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39e0457ec2d2b4a983c3fbc10989608149c95801cd935d78b47acf315b092689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286253348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353be99d01e2ddf62f150321868a918f3e04cc033646c6096b9642752fce4c6f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:1324a34d5164c61970d483eccc2194346ac044db00db0600f1517a13d155e78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eef6b99bcd6aa01e5cf0fadd1f84f804417a2aa22cd3054b2c8722a340f74b`

```dockerfile
```

-	Layers:
	-	`sha256:12b8c77b02fb73641998a275cf6ac00bf2dbba608dcd95044d60b0559351145c`  
		Last Modified: Tue, 17 Mar 2026 03:25:09 GMT  
		Size: 24.6 MB (24593807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cf20a84f6f792840ed0856e3d11d4be39be3cb96b5ce98fcf507e953c59967`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json
