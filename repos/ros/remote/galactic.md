## `ros:galactic`

```console
$ docker pull ros@sha256:f0d881da46516a06ffa1c241dd7e41a60a45b6fdeb71fe4100258f928186b08f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:02854831d159fd68b0666c827513c155ea54c0e8d3f08b2af551cdc47f423e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15b34f9aa6e3e006701be5152f2a6e7735778b5f4c568cc439b3e448d376729`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic` - unknown; unknown

```console
$ docker pull ros@sha256:21eecbb14cdccafdd9eea4494e67d0b610d33f049a9e604bf397949aa037d08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21776179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50d373342349c84c900c827495e61a0b5daf1e33a0db46139bb7ee2422aff7c`

```dockerfile
```

-	Layers:
	-	`sha256:33b77849b3a644d939b5ef2694a67a48efc5db2b4c469a34ac94599d7ed66c48`  
		Last Modified: Mon, 09 Jun 2025 22:17:53 GMT  
		Size: 21.8 MB (21758992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e414fa61cc8920d268a7f6382f4a23d43170d3a948c7f50733ed052a6eb595a0`  
		Last Modified: Mon, 09 Jun 2025 22:17:54 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a5f283e06383d5ca3740b46cfd8da263b6e4adf188937708dcf41818cacc143f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227175359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc83cfa592bc4cb5899fabac74678125039a96f07f7ef32b07d4b0dc973ab4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic` - unknown; unknown

```console
$ docker pull ros@sha256:4c5e44de34c8f5117d7258ad65472e2f1f853fce628e55dbb82e88a6c0e2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21796899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4851f085dc150a1982d92510983a60fe5251c61f79e09c487c1ae2533f48e8e4`

```dockerfile
```

-	Layers:
	-	`sha256:f9fb3e303297b47cdab714de2fe062cf76939a6b2520714d4c3d7e79024ec19d`  
		Last Modified: Mon, 09 Jun 2025 22:18:10 GMT  
		Size: 21.8 MB (21779575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfcd5600be104f04ae7e10878137770c88bcd1c10dc34d8fa236030fe3ccaad`  
		Last Modified: Mon, 09 Jun 2025 22:18:11 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json
