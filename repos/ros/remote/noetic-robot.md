## `ros:noetic-robot`

```console
$ docker pull ros@sha256:ae00f299c09f29e82f571f40ec210bc0ab6dc28b5728c4d16bea8d70db4ae0dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:d196ad972e2ca9b67cc777fbf27217205b02cd3c8086a1a1325ca836e9532051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280000464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f231966b73768df53856d1d03ac7d1464990ae56b2699ee1e027ca4dd6000a6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce9cbddae4588e8fc7fbd8a300da9a758a948cd04ec3b1368624a184de13e71`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 1.2 MB (1198681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83ce5ea8c74b3a8fcc0da7e664a139640a83469a255feedac928b11410dee6c`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 5.4 MB (5361806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10601306d61ee865bd7a1828296a8cea1d16886115c83b655becfee0c1eb596c`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1783bc90edda4ccf720a22d16ac2d0d51ddd52f7adfb85b8e78f8b55df2b12c7`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53631aa1770cb44838f8b3c2ec05c4fa0d7f3448b7902d982a8c4bdbc99a32d8`  
		Last Modified: Wed, 02 Oct 2024 01:59:39 GMT  
		Size: 177.0 MB (177026126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ca5c651827208ff792ccdfe8392da87f425c6a0a51a8da7674ad1f0b38f45`  
		Last Modified: Wed, 02 Oct 2024 01:59:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a4c7db9a2b67fc82092197aa045b09b0d18aae3b9ec8679436fb272da6a35`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 50.7 MB (50728246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7ae8432b253ca6b11586d40ec216b7f86f0dbc9ab8613908376e536dd39669`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 330.1 KB (330107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35406b7f105a6551bcad94df324847d50717d89035510b0a9e4948b93122311c`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 915.9 KB (915935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae066685f776afb0b7576f4612bf609564f75791c87d2ad2fb0e1dc0385a4842`  
		Last Modified: Wed, 02 Oct 2024 03:57:04 GMT  
		Size: 16.9 MB (16926046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:8e8dc5b44c39a5e313dd8097faecae3d38fd18f619fdd52545963c4537905876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29483752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065a66b56e58ff31db0a44a4df1ba62a1d4fb6c9a0756f9cc758184fcac5a064`

```dockerfile
```

-	Layers:
	-	`sha256:8bab270039881d95c93ea5125bcb0a0835bd4787a9b1db4742132248c7921f7f`  
		Last Modified: Wed, 02 Oct 2024 03:57:04 GMT  
		Size: 29.5 MB (29474455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ae0cb48ff4ea17dac3be583894b66372a285bac6ea641932b05d2fd11d6ed5`  
		Last Modified: Wed, 02 Oct 2024 03:57:03 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:e66a7229a6e41943d5d92e32ced3e41419860b76577ae17ae49ba0fc3c67fdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad79328eaa1883562a8fbae9d2c4d9d0385591e22c72bad81e62ded14ffe5fb5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a516110ed97a8a9c62bc914fa45ffa19c58e02fc5aa3b09f5f24402e2014fb5`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 15.0 MB (15025281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:68570be7ced8626254f62462eeb9bf9b465048b44fecc79effdef5f9832b7262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29246325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b71494b6d37b215bf54b5a742df626a31af502742d8a95164c4c62e6174c1`

```dockerfile
```

-	Layers:
	-	`sha256:32b49dd89be20c5af9d2aab4e96989d4572aa7ee7094c8a4e7e95d01ebc770f7`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 29.2 MB (29236935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb4bda7c098c3bbf1cc0d3c49cc430385167dc11410dddb7b747b5ae1e4c517`  
		Last Modified: Wed, 16 Oct 2024 04:07:07 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:77c8abc4469f538a22f701820c166b9928f0895297f8f9d2fec17400c954b909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266694841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc525104653b45a7e182f1afb90fbc7477d15937cb5398e8d9ac41688de8075`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d4290e116e35eae1f83e61d030b4d088b95b5e2c40ed078fd3b265261708d`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 1.2 MB (1198664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88877cfa8c13065d2ddb4860be1c17a12c0e4ae2c2ea0763231890ddeacf55`  
		Last Modified: Wed, 02 Oct 2024 03:36:30 GMT  
		Size: 5.3 MB (5342081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab5feed6ccbfeaaaa78d06ba63d061065b8770efc6f2bb286ffb307d46ee61`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220127cb75259289f6f01775c6e6edcf220b331062be4654dd6516eefd4df547`  
		Last Modified: Wed, 02 Oct 2024 03:36:29 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe60eae5591c9e6979d96562bdee2e70645f096510a26fe57899e826966b977`  
		Last Modified: Wed, 02 Oct 2024 03:36:37 GMT  
		Size: 171.4 MB (171434164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33047cc09a47eca1deaeb10981a2b592f2f8bdcf137e3dda26a45aa9001b787`  
		Last Modified: Wed, 02 Oct 2024 03:36:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da160f1f75162eded88c8ae9df843e3883fe8e2f75764322a67b48f59456e440`  
		Last Modified: Wed, 02 Oct 2024 06:05:55 GMT  
		Size: 45.0 MB (44991209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e3b25ed09c43a8a64a558ecb2dd4c86c266bfe0bdf77236230276d1e721efd`  
		Last Modified: Wed, 02 Oct 2024 06:05:54 GMT  
		Size: 330.1 KB (330097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e6709e7835c2d3f13da588996a2ccffd912de71d30557a1b75740e25970557`  
		Last Modified: Wed, 02 Oct 2024 06:05:54 GMT  
		Size: 897.3 KB (897295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d875c441080e678d9cfd1ae64245d345cf586ac5c8ebba4e0fedbecf8e45af9`  
		Last Modified: Wed, 02 Oct 2024 07:23:18 GMT  
		Size: 16.5 MB (16525273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:b364b5434007d1435e0f27e4775fbb2f2230f32d66b3b8da17d87410c9fdb137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29432966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e64b3056bf8789003b5b51b2639bc8a4565c018445d2ca8ad0a57766b7498d`

```dockerfile
```

-	Layers:
	-	`sha256:b06d6c16d3767be2a949422443115af6b3a4f55870ce204d43a24ace0464da21`  
		Last Modified: Wed, 02 Oct 2024 07:23:18 GMT  
		Size: 29.4 MB (29423589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7753e4788386c2d7dbb6d52c4286e52cb09838e8e4e6af16f4ed54d9f611e2`  
		Last Modified: Wed, 02 Oct 2024 07:23:17 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.in-toto+json
