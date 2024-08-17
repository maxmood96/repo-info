## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:f23afa26ab4b34e0e5827f905d5b8e4494c5a5d58b1b015607194cf02d9bb221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:379242c95e2fc0df3ff873e7dc4cb8f3897aa799c34c4f898da31e870d9aebbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267704187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f697ea9cc5a8853a2279d11acebefd2130b382f4a00a29042021cfacc84e9`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b6287828e4497dec4d781c2674ba9e55f149423ae252f89c62bb84b1706d19a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075206c2478e07f068d4501dbe416605a5c9910f3d68a5f8c4f7095de507a623`

```dockerfile
```

-	Layers:
	-	`sha256:9c8044a86c7e1b23b681096d75a5090eca18d054c46acf0ba095dc28e8c7262d`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 23.7 MB (23676936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2e2da58e9c10f8f9463fdd00b53f5cc33acab8e115a3d6583dc25f70163896`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:56c0d7d90a4b206c1b726b56aa535ea9adea99e187ab26646ae0c3ccc0aa8c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260022791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1281b31359c8bc875f81187fad1e6c9c72ad37fa7bbd36a883fc396c619cdc8`
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

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:60f667f1fcfd77dd7d02dbeca3198c7c80fd5c02bd866fb1a26c648cf9fe423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23574381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3252b6ebf92da99d0df6f2af925f6dcfdbedf86bcd9943d32b1942ec7890b`

```dockerfile
```

-	Layers:
	-	`sha256:d11eb8493b25cf6a9a804c33cc3d5b0ff6f97eca723cbd7f0023faa2d34771e6`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 23.6 MB (23556918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7545fe198f2772c095cdf780b2a0538ad4402b8e27fa23dafb6ba1034eb20164`  
		Last Modified: Fri, 05 Jul 2024 21:14:48 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json
