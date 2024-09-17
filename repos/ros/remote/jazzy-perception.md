## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:640ea78cd08cfc6b3fbb32ff8d0b7b410263c57ff5f2e9230cc1dd47c31b57e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:562ddcb7cdecf28139f141852b1590638f95cbf3550c2efeca33c9fac234bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624913772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1280adcbe207e351aa67df3fe1862fa1b73ae9341dff73ddcf69542f5976eb94`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76a4ee6bd37d6f59d31f5c887311e5e357f57f4e71fc7509132768a58e399f`  
		Last Modified: Tue, 17 Sep 2024 03:03:15 GMT  
		Size: 323.9 MB (323897780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9396d083c18356d3d6907cae04f955abcc499e76c50c8cebf489d477c9e7cdf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42092885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea80db29aa0acd47a1e183b00143c3d83c923ea15a3533fa1e406b709378227`

```dockerfile
```

-	Layers:
	-	`sha256:f0afc267360d5976558e24e87bbbc9c914b64f50ddf337e97bdd4a38765e0d71`  
		Last Modified: Tue, 17 Sep 2024 03:03:11 GMT  
		Size: 42.1 MB (42083231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e640e9b7e8daa2964fce3ee3bf9a7e8515f24646591c13faa363d1f0f297812`  
		Last Modified: Tue, 17 Sep 2024 03:03:11 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8eebc6ffd92314b1833e06171223f52f9de798c40b8dcc1fc3559b47d81eabec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.8 MB (567794628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3286e660df0145c72c9652d4e0e40eeb9362e2099155ed7f76fb5d1e9f1c5109`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7125b2360b0a7e967429934d8a8682aaa8dfcff559778fe75399fc28565fb4`  
		Last Modified: Tue, 17 Sep 2024 08:07:13 GMT  
		Size: 277.0 MB (277012315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:288b279c7248e078d722abf741726efa283e0727c1d3c9e7ab35d9e78e4b11f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42091339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d51944033316ffd311477dea436701e7965ffefa3ff6daef68544ab3daeb67c`

```dockerfile
```

-	Layers:
	-	`sha256:0dd99915b79df3a9f0747acc4f24a11c6d74af0f77de58018e0c23f39acb918b`  
		Last Modified: Tue, 17 Sep 2024 08:07:07 GMT  
		Size: 42.1 MB (42081324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5508be16bf7e9178906fb10a9df1073eb447bc3e4d0240010ae06fd9fd1eff43`  
		Last Modified: Tue, 17 Sep 2024 08:07:06 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json
