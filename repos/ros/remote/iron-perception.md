## `ros:iron-perception`

```console
$ docker pull ros@sha256:71056fa056321590c7d980feb822afe94fa514ff69f0fb5f09bad41f7305abae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:b11908a6b870acbba473bafea86168a78fad5d7c22c8dd1913e06d109e6fb7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (960027971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99de75e0f15325ce0e9a57b3b15aa176d59049f94ebadb25c927377b74d9d795`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d5fab837b49bba793141aff686b0c6f68bfec9cbf399e4fbe0b9f485a9a36`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 85.0 MB (84961563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0547d9968b62e61f578a202d34e1d8fa2ab3d1ea00374118b5155eb554a46`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 315.1 KB (315111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3d90fd3b189da91d9eb321cff21faafbad014dc98d94c03b50f6cf32d01bf4`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf9f1e81fe596d17c20e89ff3648760dba253d4a63cf4a6da095a95f2e530d`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 23.7 MB (23737116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b516d5e0a7f715646eaf84f4372d78cbd699a5511c506141e9adbe309540977`  
		Last Modified: Tue, 17 Sep 2024 03:04:56 GMT  
		Size: 692.3 MB (692309404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:86a44a4ecde0aae3f295a0797bac0980b64f6878942e7689f1ed518bab05c6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58260122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f8a9a8a3193c12d124baad32de3c05777ddbdc1207edd7bf283e741b43813`

```dockerfile
```

-	Layers:
	-	`sha256:e1b18f0d90e3a70c3bc9800aa5d68150b338405083d7e383deb683b0684a1b86`  
		Last Modified: Tue, 17 Sep 2024 03:04:47 GMT  
		Size: 58.3 MB (58250482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020da288a7eb976b41ab3d4de13868dbe77dd6cd14cea558e0907367d3e26207`  
		Last Modified: Tue, 17 Sep 2024 03:04:46 GMT  
		Size: 9.6 KB (9640 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

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

### `ros:iron-perception` - unknown; unknown

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
		Size: 58.2 MB (58246875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee3e6d30d8cb2253f5eb15b99dc024f7005f8b62dd78ee6c2f11a8a00c995c0`  
		Last Modified: Tue, 17 Sep 2024 08:00:08 GMT  
		Size: 10.0 KB (10001 bytes)  
		MIME: application/vnd.in-toto+json
