## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:96504268bed5d2f9c2f62b0a87caecf894048e9ca2782a4059e6e5ed48df88a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c2921595dd6fa6b17f196f7bdd58e8273a5fc5ce48596c3f1c9034a8977e7dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (960010120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c651aa68c5d93e322cd24ec614cff7cadd600abb0cbee44034c0fcf40285e04`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f7236f93b78a4c5838ad92c9a6bd7e07011f128ca1f1a8c982b8de30a776a`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 1.2 MB (1214729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bebe6781c366f7c1fdc19b776fb1d789e4bcadbc43d40671685831fd3b23bf`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 3.6 MB (3624541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b74d1b6c5ce02dddf579d8b0e5b7af7f7a8e586f96f6e4403ce1b253c4a30`  
		Last Modified: Fri, 05 Jul 2024 19:57:26 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177212e66b063c476b2f24bae2438585fdb791a9d5ca4f4ffb967a56dfcdeef9`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a51e4e3fc35489d611b105db96d3fa487d2174d8d96917d3832b883a1194ab6`  
		Last Modified: Fri, 05 Jul 2024 19:57:29 GMT  
		Size: 124.3 MB (124329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047335e2d0fda3eb0e56df44fb15d63cfbee7c96c69d558d1e0b3c133737df32`  
		Last Modified: Fri, 05 Jul 2024 19:57:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0d933854218a9e1460ba2599c3b9f8a08975b166695d685a24a9ccc9229702`  
		Last Modified: Fri, 05 Jul 2024 20:52:52 GMT  
		Size: 85.0 MB (84961292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f9bc9b53a6d461203c68dbe75e897f501b776e81c27943556241bd3e0dd484`  
		Last Modified: Fri, 05 Jul 2024 20:52:51 GMT  
		Size: 309.1 KB (309112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4a6a021fed9c7b5d074c6801e8138520fac50ac5132bf8bc45d0f2fbbeb3d`  
		Last Modified: Fri, 05 Jul 2024 20:52:51 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77930caaa34d87ae3b3e977b402acf04a35fcd702c6472c2f5ce9de3b0c98db`  
		Last Modified: Fri, 05 Jul 2024 20:52:52 GMT  
		Size: 23.7 MB (23732565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8246b305cd605a044925b9f5ba72aca36b518b1e301e23c271f0a9e221182`  
		Last Modified: Fri, 05 Jul 2024 23:00:09 GMT  
		Size: 692.3 MB (692299568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:8017250de85f18ab5d14b548a621714e0d81794de1fd8d4e6fa18f12330c03ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (58001049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd6156c46ef5ddbf12c175ea664ef159713d905e6418603af9711bd0e0296e6`

```dockerfile
```

-	Layers:
	-	`sha256:8c80491dd3d4f74eb42078dcdf5e084037e9b0257f2921d186ccc65d66806868`  
		Last Modified: Fri, 05 Jul 2024 23:00:00 GMT  
		Size: 58.0 MB (57991409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f8e49b8b7194a756720b5e78537d8a01ca5e538d4de0780dedc00ef3eeb815`  
		Last Modified: Fri, 05 Jul 2024 23:00:00 GMT  
		Size: 9.6 KB (9640 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7da21c2f7315db6b1153278dd6f47595a58b6aa195134edd1ba2f9e8029e4db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920196188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd11ed6900f7375590f563df50b6d7c5753208406b85f085ef857b43f69a0314`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:e0a65151261e16b95c42cc0f2d0cdb917819146f037a242ecf1ee7b8de2b2ddd`  
		Last Modified: Fri, 05 Jul 2024 20:43:47 GMT  
		Size: 121.8 MB (121776520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c984738d175b26d50ed03560182815a089083eb2a11aa0ab2517627701d45`  
		Last Modified: Fri, 05 Jul 2024 20:43:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d69fd9744647d964d1e8f768f77146a429bc8e68f4b23999fbbfd75418d45`  
		Last Modified: Fri, 05 Jul 2024 21:14:51 GMT  
		Size: 82.6 MB (82644201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d035d7dde10215aba73591f6b955de11b855ddc4ee8e03c29f299a28eb56712b`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 309.1 KB (309119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94d3e4e9957aecb6ab51a45401c5b1743891d5b7cb211e5c53d118cac076de`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6457c9d5cb93d7645f227282b7cd5c54fdfbe843e587de67969dd5beb7ad93`  
		Last Modified: Fri, 05 Jul 2024 21:14:50 GMT  
		Size: 23.1 MB (23117144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69799820628b45d45a6b4bd29d1e8fff4808119f3dade1703e3f5a01d901923`  
		Last Modified: Fri, 05 Jul 2024 23:42:16 GMT  
		Size: 660.2 MB (660173397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:c4d14ec735e30d45167679ede10b2c8bb8e8d9fc3f8abef855e2ccdbda10b9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57998805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb34605da1df7939e9b3ce404fdcbf7b0d68fefbc1450a68316814a78a1c58`

```dockerfile
```

-	Layers:
	-	`sha256:96d16b69f5c7b95d63887fb880043916aecbfafe108052815d1363a14151963f`  
		Last Modified: Fri, 05 Jul 2024 23:42:05 GMT  
		Size: 58.0 MB (57988803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb26277d9dbc3b03e36ab4f713b6c90ac577dee24f8480666427609ef50c89ae`  
		Last Modified: Fri, 05 Jul 2024 23:42:03 GMT  
		Size: 10.0 KB (10002 bytes)  
		MIME: application/vnd.in-toto+json
