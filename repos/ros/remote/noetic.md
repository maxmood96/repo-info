## `ros:noetic`

```console
$ docker pull ros@sha256:2c286e291d9a363530cba6cb443d58fa7e1595e1846252f19ea837424ef36af3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:c64e618fe3f69ee3215a13e75af121030f5f2f4488c7946c7f30d0e3b5d178e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263074418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b0870daa11b6d9466bca105cac304479054ef23f54c9e852547fb2a1ac034c`
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

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:9ea2192ed22fc55edb39258fb4b661bed350aa507a8db70d61dd8c1c2430fc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27600780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfd49779650ba0abaf75b87c3c1df5267b684cc8b9f3a0265cf9efaacb87afb`

```dockerfile
```

-	Layers:
	-	`sha256:e72e5164e39a8570cd3fa8358feb84fec97428ae31141724867c75afe98590b5`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 27.6 MB (27587123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0418fabe623fcfafc4fa0ee2557167ade6720b6d3064a54e1e2580f787e156f`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 13.7 KB (13657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:13681d9bf67dcd5c953b9aa69716d4a20b7599de86500aca341af37a290a0da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228289225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617da7749310a23ce82afcaa1c0ffcba812561090d21a17aab9c317100f7792d`
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
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
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
```

-	Layers:
	-	`sha256:11eda96b18d1f3db85ac2aa91b88e0f8afbb12b21c50d6dfa06eec4ced4c76dd`  
		Last Modified: Wed, 18 Sep 2024 05:32:52 GMT  
		Size: 23.6 MB (23619920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5e426c7b7c694def02912292361e2695558e37ff1afb19f3d251479df029f8`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 1.2 MB (1198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdf3697de627e9d1ed3bb19927623ab4c49cfa682d7fc8a960832f73a7042f3`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 4.5 MB (4487307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3128b56544232e4c8e974d146e599be7050e87e5c52da65e4e5d4cdc804fdc77`  
		Last Modified: Wed, 02 Oct 2024 03:51:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ade4de2e774de5ff58e31a47d1c5a493c2793085116b0368893652d49289b`  
		Last Modified: Wed, 02 Oct 2024 03:51:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0595a66a5286ca6f2c09ddc1480ec9384b51bf3f0a036ee5c7a35fde1ded9159`  
		Last Modified: Wed, 02 Oct 2024 03:51:43 GMT  
		Size: 157.5 MB (157512590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114f75e546f007a1cdf08d0e0edbdec7643a3992321e83099513616133e099be`  
		Last Modified: Wed, 02 Oct 2024 03:51:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f962e252dde920852b623a9610a82007c1e2bc3586f1d866db1ef66a75528`  
		Last Modified: Wed, 02 Oct 2024 05:29:56 GMT  
		Size: 40.3 MB (40291263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108a48ce9cbbc1f3bdc88f635100ce184945ee6b1b53fb957ac3d3e895b932b0`  
		Last Modified: Wed, 02 Oct 2024 05:29:55 GMT  
		Size: 330.1 KB (330100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e320e67aa0c4eb1e98de81ca7303a3b6f6035001065b42c2536e3d85c5ee9f`  
		Last Modified: Wed, 02 Oct 2024 05:29:56 GMT  
		Size: 846.9 KB (846857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:8e66fa06df9764602ad12f7a7462cbf563c8e6cc4474b83c3a2a6a5b6082ca90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27364229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de50517a1b358a818270d34be88486fba5b8719592de9f0de63429cfb74ba09`

```dockerfile
```

-	Layers:
	-	`sha256:f1ac06eb320e3d5b021d696b712560f7d1609d763a54945ab7ef26b7e8c1b3c8`  
		Last Modified: Wed, 02 Oct 2024 05:29:56 GMT  
		Size: 27.4 MB (27350478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50fcabd011b234c2b82d063f17840e0a7cd60db5b07a5b163e239ff24fabc9b6`  
		Last Modified: Wed, 02 Oct 2024 05:29:54 GMT  
		Size: 13.8 KB (13751 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1097bb6b6c403466e59c88c999a9128b822e12431246b0786f66abde7e8b3a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250169568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d40ebb1bcc1f747ad2854c65a34df27089938cf4458d540cda8c78bfc46fd1`
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

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:5cf5aa75d334e5d687c3b631fb4aeecc67a8a7b8074622bb12c8fa50b33e438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27551188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69583fdb96cc616ea6e2f05b0bdbf2e5f507a47f2541103fb9c0f895681c1ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9ec7aaaa89c76387a1db0cfa3e727c2fdbd69d4f197d231875cd6297db600082`  
		Last Modified: Wed, 02 Oct 2024 06:05:54 GMT  
		Size: 27.5 MB (27537409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ebc42c093b6ca617959789f91c7e7b4e1e143e22e5de2526f47caaf6beecad`  
		Last Modified: Wed, 02 Oct 2024 06:05:53 GMT  
		Size: 13.8 KB (13779 bytes)  
		MIME: application/vnd.in-toto+json
