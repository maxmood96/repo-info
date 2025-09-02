## `ros:latest`

```console
$ docker pull ros@sha256:23b55f4f311efea4323d848890e0ce9dddc1a16280b7ed994514aeeb631e6808
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:7f115cc6266a06edac7e619293ce1a9abc747c8e3dec91dddfee7d68ffadabcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295897654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a3b0409bcba5cc95830549d58fc7b6d00f582351301d2211e2de7274c47554`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad268d3577575b8a090cd6e684e1bfe2743e4ff225fd68d59f6cc8d1311efc1`  
		Last Modified: Tue, 02 Sep 2025 00:13:52 GMT  
		Size: 683.8 KB (683827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8905021a0e9d1029ab7dd7f84415090e39e65ca21a7df47ef3c9979f86d6f8a`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 6.7 MB (6746681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b374353b323cb503e72f9217993e9545747c2635f474858cf301ab4eb3dc7e2`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 94.1 KB (94067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948960a889906032c1cfe6c7576e66036370fc2303edc1886125832bb4feb838`  
		Last Modified: Tue, 02 Sep 2025 00:23:50 GMT  
		Size: 120.1 MB (120091608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2cb1a3fd6fea1facb4eefd901cc55e8b4e196e5ece372ee5fbe3602870e7c`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610e404c741cc3157322e2ddcca15d30da2fb7f346eb3465a091b20317ca5878`  
		Last Modified: Tue, 02 Sep 2025 01:12:32 GMT  
		Size: 110.2 MB (110182606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779737f31af27db752ae2b99cf2d51c8c6c371e8ccb1df300402aac7393fd530`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 375.5 KB (375470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c14724f62e3a3f80af2cc44890e7744dbdfac3a41424fa477b97263802bf909`  
		Last Modified: Tue, 02 Sep 2025 01:12:23 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bf222367561b42fb0e9b4a01be0b7f986ed37fd538e5bb7df4223ffe7d8d22`  
		Last Modified: Tue, 02 Sep 2025 01:12:28 GMT  
		Size: 28.0 MB (27997635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:b656819aa97d6a1d8810e8c976997391ae2f9f0bb44bd3a2059dd5d477c1634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6320738f023d5c7d07d28e7a0513c9b2f3051e213d755813ffe3b99b2f043caa`

```dockerfile
```

-	Layers:
	-	`sha256:f32b874de7a2e8c44b4a586290104742135a13db017fcef4ecea204b58f97d94`  
		Last Modified: Tue, 02 Sep 2025 04:17:37 GMT  
		Size: 24.5 MB (24543450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da361f88e5269782ba53e32a6bb5556aedb6448fa8c75da47700407ed704ef05`  
		Last Modified: Tue, 02 Sep 2025 04:17:38 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ba8c12a02611b26ab22fb1fba24e7ff64fb96b1e6f0d5407f1c1ab523981f8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284340187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c706a0ef9572b767022547d1e83a2457e309d7e6223be11e32b3dc27303b7957`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1aeeb021ff56f6549713871ea035936891c67787fb388f08e69e57ccaa5f2`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ffa2a8671f1746a19c7af89127b62a1f22836df01caa93a61d61b0d2574661`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 6.8 MB (6759788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a01a08d6a7cb15e63953b7781299b8e80e32583b1030aa55d13094df1d2d7`  
		Last Modified: Tue, 02 Sep 2025 02:55:38 GMT  
		Size: 94.2 KB (94161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4efba9b395ff1f9acecfa58641bb667b903285e0ef042738741ad9d8159dee`  
		Last Modified: Tue, 02 Sep 2025 02:55:47 GMT  
		Size: 114.9 MB (114876950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fdfdfe0ba6ec7783a4b4e7f923dd952363d4366df0d404978067fee5587ee6`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf89c06fcc3afc6b2705366cc8636dcd88d0564a3b7d6ba96944b71cbf539e`  
		Last Modified: Tue, 02 Sep 2025 05:38:46 GMT  
		Size: 105.6 MB (105590903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249975dbdc1c56dadaeb2292cda4a4a82a40bcf1f1536f9280c6d1a0abb0d6da`  
		Last Modified: Tue, 02 Sep 2025 05:38:39 GMT  
		Size: 375.5 KB (375473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ae6d125f1a74507ec8a50bd0a8ae712b6f2ee8398d019893f6bb18ac44ed74`  
		Last Modified: Tue, 02 Sep 2025 05:38:39 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6301073d1fc26710ed27ae5bf7ae936b48d07b393f21a5929e4474dd7d46a3`  
		Last Modified: Tue, 02 Sep 2025 05:38:43 GMT  
		Size: 27.1 MB (27096111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:3f84c3cbf559e25bcd1bcfaece863c948fbe978a47b16589d493fb899310924f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24582536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a693f10529ecfe6cc86a10d99a674039f8261bd06e533c9718a0527ba9cfc7`

```dockerfile
```

-	Layers:
	-	`sha256:ad028ca341cc49d1263038c44ec33bd051c8ebda1b4615c7a77c5413af4025b5`  
		Last Modified: Tue, 02 Sep 2025 07:17:48 GMT  
		Size: 24.6 MB (24565723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76081357ac7a974ae033c371b9452cf838bcf959a62553a8ecaeda2a782d07ef`  
		Last Modified: Tue, 02 Sep 2025 07:17:48 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json
