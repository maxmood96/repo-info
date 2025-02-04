## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:6fe59e946b4f4419fd2c16f6d4044b0c904af091f4f061c53035f3c14121fbab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:bc340a3623ebbd3fe5b54c34c93c08b4678162d06571ac9cecc2e22852f22011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.4 MB (960393789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dbff14113ebd665f83d451f89f83f9809940a0470ab6da67f6ec6eff650ba9`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526137aab8eabb030282d4cd36a82d84f0c98f7e226cf70b0a70555c16350261`  
		Last Modified: Tue, 04 Feb 2025 05:26:44 GMT  
		Size: 85.0 MB (84977086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e786d9035575d521ab8b98957006a642cdf3e9f87a7cc100de30768e0e494`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 321.9 KB (321949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449373c6d3c93d44e06855012381e095988cc78668a7d4e2295d11c598a245c`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86111058d79ae057cc88f50bad018887961928fe6dd06ef2cc66f303b0015c30`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23735561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94dc45dbdb0078da869c53a65178d2d3219dcc8424b074f058e789baa6e6b2`  
		Last Modified: Tue, 04 Feb 2025 06:18:16 GMT  
		Size: 692.6 MB (692630322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3c89255c9843aee1e48386feaf02c878684785c8fbe4b7530c51c5ad44c8bd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58341315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62dae043b9ba3c9b61b588fc794db708ef7c23f384f49aea7c2404c165824c`

```dockerfile
```

-	Layers:
	-	`sha256:be435e71cd61a6de7cdf9d95b7433d6f5e6ca4f82b9d309356d9c4a2454ce7b1`  
		Last Modified: Tue, 04 Feb 2025 06:18:00 GMT  
		Size: 58.3 MB (58331640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67565e969885c8068adb136f3586258dafdb8af3c56373d7132a137b939a6ab6`  
		Last Modified: Tue, 04 Feb 2025 06:17:58 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:114a133fffe1db7d3dfa05cd821a1741204968452ede0993fe2005f1e1ed6982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920236423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb9882929f140b730cc82c95e045d9fada684c65df8b860f7aca3c577478785`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7dd201263c103c809e1c44853e0636966888f2e37335ba2e026f35dafaafb2`  
		Last Modified: Tue, 17 Sep 2024 06:13:47 GMT  
		Size: 82.6 MB (82646665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f0f63fa981ec33dc63f4267e3f21c9f2816ea1bb26acc01a6ded62ef00af1`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 315.1 KB (315114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4c039d165d6a20ea24e5ae06e4057f612ff7c5c6f87a657205ca0300213ce`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f4d1352e2286892bc738d595b438bc1147d080ee49a6c207153c9ccf4e35d`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.1 MB (23128446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d806dae4ec45dfdd497ba2fcf284d15f981bee138fa71fd78bcb0235e96fc20f`  
		Last Modified: Tue, 17 Sep 2024 08:00:22 GMT  
		Size: 660.2 MB (660206262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:a794980dc98b5c7b9fbf4043a6aa5c95f00f3ec596a162e7e245634f7b2d330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58256876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648167f650d81f0084300670e41d614ab07760573efa8d7a1734d51d996f3b7`

```dockerfile
```

-	Layers:
	-	`sha256:de474500ff35deefa1abc0933752aa38cf597e1af65579be4580e9facb884dec`  
		Last Modified: Tue, 17 Sep 2024 08:00:11 GMT  
		Size: 58.2 MB (58246875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee3e6d30d8cb2253f5eb15b99dc024f7005f8b62dd78ee6c2f11a8a00c995c0`  
		Last Modified: Tue, 17 Sep 2024 08:00:08 GMT  
		Size: 10.0 KB (10001 bytes)  
		MIME: application/vnd.in-toto+json
