## `ros:iron`

```console
$ docker pull ros@sha256:305188f4e1d299ed11cb6dbd35f307837df56b8481848d94a3d41fa0f8d710e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:632a5aac59584ab5bb0e06d04a5e39418ebf2353236fc015daa44a4b040b58d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267763467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b59e7539bea06cab6e83e21efc0b8bcd0f082a25d2b72ac99056ee573c6b9`
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

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:0f2a5c4bd2272c4809de2465576673b7e95bd96520b16ee5b47843a9bef7a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23735695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdb4edf36e22a3a5e107167f9c1cb525396ad29994ae7f103df6508c358bd83`

```dockerfile
```

-	Layers:
	-	`sha256:06d23bdd842d459cea3aaa27f2e94a10035256d473eba4ceec69a7c08d68ceaa`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23718572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246f9008e3f1ac54635b14820165dfc6645009b893dcbbc986ec4c678bb7f41d`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 17.1 KB (17123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:923dee9792d1ac0772c83ea00bcea1fcecc3436f969148c817ac165a3b87088e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260030161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaae715bf4e1ac4053be3a3ce01be416bc689a2b6025438170dc8b4c6a2fba3`
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

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:7d5af0baeabe69e767955d95397ab04bb27e2c12bb2326de62c29352ead7486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23707637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736281f35081f119a4156a7645a4a422ac8a26270e654aaf3e56656648b92e2`

```dockerfile
```

-	Layers:
	-	`sha256:508076939eabe19b1b849463536d01de387d086d08229596d83872bdffd9f0fb`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.7 MB (23690174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c567ff9e8346fd963c339e60aa4fe17485f2fee1d54ba9c9ef80828de6f959`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json
