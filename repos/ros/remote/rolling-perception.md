## `ros:rolling-perception`

```console
$ docker pull ros@sha256:f104e99335bba74e93fa04745a284475db99e6f5014454b845cc38aa8965cd7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:2839397da38012606d3f6323ba5dcf8e34a1638ac8f383b087d900079c05fc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076612279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b9ded77eb5ffaf74c10277c85e7fc7223f60675b3d9aa0889fac13d76cbcd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f9f16d221b9a193b1a080b2673609f80f64ede41f3f81c206698e992ac9fa1`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 683.8 KB (683811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88f57e92d728e668d2ec085a2a883a4a34de7358c5ae73ab669d9d0dbd34242`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 3.6 MB (3563720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46c7bf8a560bdecd06b706f996ae07581fd85ea16d14584cfa8cec8aef4d2cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fb3faa63f0489dab4f0a12e3b29eff9ce565faa7156b7f3d9055ed3ba6007`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f2ce02ff513de028c65887ea53630d7a99c801a501871898ce4c97695115ad`  
		Last Modified: Tue, 03 Jun 2025 13:31:05 GMT  
		Size: 123.3 MB (123309297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434c602a34bcd520302797433be6f8c41329d0a12bbfced7922b0ac74276902`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80f66809e8d851621b51dc33d9630198a62ce80e16f7feab75496a1f23798`  
		Last Modified: Tue, 03 Jun 2025 13:31:02 GMT  
		Size: 110.2 MB (110181616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3999dc1f9ecc560440d5247cd73447037c04c5053ce5b1f73f8f060a0ebe9e7b`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 346.1 KB (346125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b40755095da1c5c4d3434a4e38fe190acfc281ffa2d0da3d71cbcd14a05d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e955cd61a0672a29fcb7c5dd1cdb21cd12c405f549aee9fc4807c6eb9fcc97`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 28.0 MB (27969498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3f4a15876b42ac2b042f88984f0d71a9c20cd5223a4275a33d3ed30c7ab0a0`  
		Last Modified: Tue, 03 Jun 2025 11:13:46 GMT  
		Size: 780.8 MB (780837380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:eb57c64f3e5496e82beb293b31f2efbb88fd3e577efca206c59924d0fe04d11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59835941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d8d36169ab341667e42231b90bd3feea805da0d3084136437af593731f86e4`

```dockerfile
```

-	Layers:
	-	`sha256:63435aad3b4924b13089751704f3df02103f108acfb046c167abe47be14a781e`  
		Last Modified: Tue, 03 Jun 2025 16:17:54 GMT  
		Size: 59.8 MB (59826232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdeac60e921a49da7d68fb7efcb74938db20de95b82c40aeb8adfd27487d8e9`  
		Last Modified: Tue, 03 Jun 2025 16:17:55 GMT  
		Size: 9.7 KB (9709 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bb18e1a9fd573169da13db429ec9ab386fcaaec9e50aaf040bbfa782f2cae9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.2 MB (975221972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bef50aeedf5077e3c0e517b57ccfac30d5f3fb771338eb4789fecd1229a776`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3182864e52220424abbc2ed14f34194efd7a8651cbd58c9013d59badb6ce10bb`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 3.6 MB (3562006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30261ce10ab5a3b7dce5ba78a1a951d5652cbf529e166b904f1bd8067ae7ab`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ede17908e49502f7fe6ff9399c21b4349b35f3533c331faba1f2970ddeecb`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f4c48fa47caf9afea890bd995e3397de16a54fd781888ecbaa9b5688368a9`  
		Last Modified: Tue, 03 Jun 2025 14:19:52 GMT  
		Size: 118.1 MB (118081461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a93e6dc2b884b097ad111c9c09580eebb409db03ba379e3e847dc36468a587`  
		Last Modified: Tue, 03 Jun 2025 13:56:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111fa49d32c398c3cdb3a803afd70fc1e29cf19976c5f78d4abee039f51d5eaa`  
		Last Modified: Tue, 03 Jun 2025 14:19:55 GMT  
		Size: 105.6 MB (105595311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ed73042d776eadb29364537e29fe84b0364092210fc1bf8040a7d844c8092b`  
		Last Modified: Tue, 03 Jun 2025 13:56:39 GMT  
		Size: 346.1 KB (346129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0bd3c3945caa5d7a8dbc804f7e2a188e63f662b849c402e7f95a56a190ed`  
		Last Modified: Tue, 03 Jun 2025 13:56:42 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405f57d0b137d304f12eac8e652319d0198fa221a68bc4301d89673692609d1`  
		Last Modified: Tue, 03 Jun 2025 14:19:45 GMT  
		Size: 27.1 MB (27061888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5045c87789dbff7da9b8aa07affecf177a631d508a886a95fecebcb159a96`  
		Last Modified: Tue, 03 Jun 2025 13:50:17 GMT  
		Size: 691.0 MB (691033792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e838a42cef675ba215ca8ab1b73fe1e70c9bf6adac44623ce59258e61060fb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59787687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3677c04297ea36ec3055c7b90745387fcc8cddce622dae5c71c29f736118aa72`

```dockerfile
```

-	Layers:
	-	`sha256:1fb6c37bd0ec74662faa6900d4febd665762e5539c690f08da13a7b972c7a29b`  
		Last Modified: Tue, 03 Jun 2025 16:19:56 GMT  
		Size: 59.8 MB (59777897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07091e2af20f57227a2bea69765b15a5a201a80d981d58ad5df60d9bf5b301e5`  
		Last Modified: Tue, 03 Jun 2025 16:19:58 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
