## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:1ad47dc6fd722e08c5268f95796b9e9478491f831c33447751cadc058a3453c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:54d640ad3692f96a975b86f6e5420161b22da938b9dc95de384c477725dab7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082043008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d9827f6eae5901e23e8bfe702cc8694f7979ff64b77994628d3e2306b4dcd6`
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
# Tue, 17 Mar 2026 04:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:5299b46a39e7b4ab4ed2e084669a311ad188e3fdb3968fb53ee5e074b64bf0ff`  
		Last Modified: Tue, 17 Mar 2026 04:20:00 GMT  
		Size: 784.3 MB (784305067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:020b8a7fc63cc04d5bb9064a2b42916472f7fca79c026c206f928b9e67af45b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60737111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93073a2eb9d488755717f088fa95f283d09e46c2ce87b070d5d047f39cc24e0c`

```dockerfile
```

-	Layers:
	-	`sha256:5fb64c9fe5264ca00e3ab89dc1959a13ac0fe67bd74622a0715ed27fcf7336f2`  
		Last Modified: Tue, 17 Mar 2026 04:19:48 GMT  
		Size: 60.7 MB (60727772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98e1791b9d513bd6bd97e8d8891300aafb511385f0475d5ba635f61c3a12118`  
		Last Modified: Tue, 17 Mar 2026 04:19:45 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cde737f692ba72693f4f5853a886c1d4e5d44a25d3379d82d35984ae0b0be87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.7 MB (984708218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825936dbcff8e6cf391ae63acf18f3f09a0b512b53abc0464b03d8eaa6432703`
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
# Tue, 17 Mar 2026 04:15:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:312dbd512c95ff5845350c2ebb0ea02142abde88f5735ff1f1404ace81bdee14`  
		Last Modified: Tue, 17 Mar 2026 04:18:00 GMT  
		Size: 698.5 MB (698454870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a3513a767ae00e18b2901020cca6227ffe591996b8d0ebbf8f7856b450054dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60667699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fa5c404a5a1de50925cd89f20f1de8ae748c608e1a4f148425b5c65b04aac`

```dockerfile
```

-	Layers:
	-	`sha256:e41b2e555c0ace0eccba9b13d88f60f0dd47291abd4e573a24fe13f5dce538d9`  
		Last Modified: Tue, 17 Mar 2026 04:17:48 GMT  
		Size: 60.7 MB (60658280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3d8b07409863bffdb1ec3a3c518386e0ca58a15b74ae50375884bfd5de61d5`  
		Last Modified: Tue, 17 Mar 2026 04:17:46 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
