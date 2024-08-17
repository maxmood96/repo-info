## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:0661cb2cfca4606b7c19322af66c6bae96e6df8feae726bc352b5254849cc8fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:594cba7093a34ae4c3dcfc4c92f9cae3482a340b5862ad1ec7e8efc5a98f2877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298412289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f875aa41a6f0bb901afb4b04401d77494a8cf2f766ccb3c7ee14c62374825055`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:059c1ae31ad97fa76a05ab9b31dacfa6b20aba6aa7acf794856ef7780209e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23845572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c660aab28280c69329ab186d67edffbac0ca48b4d3e1ac16e4131cfdfcd051`

```dockerfile
```

-	Layers:
	-	`sha256:8a27cd29d74c2296921f3e278f7c6c176fad2d69ad912d0aea38a6561ef15ab7`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 23.8 MB (23828433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af852a1c69e2e47506fdfcd1644355e2468a37f02bc272e7a5780a5380df5af1`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f92b2c25f35dedad6c9437e4e8270ea63b00bd0904839533ccb29be7d6f63d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288361228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8517f184577fff80e67e8c6a16ee3f657bd69d40798a75642835a2ff9c21111`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9c04e2bffc1ed794fb172146ff902e16b2168278b07cf37fa39ebba8e09d`  
		Last Modified: Sat, 17 Aug 2024 04:02:49 GMT  
		Size: 117.3 MB (117330906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97270cb5d2135d6378730d2c10ca4fa7c82d05d3108eaef2bfec60d3b45662d`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccc3275c07ebe6b29dc19cec2423d400043f0209a700c10aa48ae01a022b46f`  
		Last Modified: Sat, 17 Aug 2024 08:17:30 GMT  
		Size: 111.0 MB (110952813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f49d0f5ee7707c7525730708029ecc6d65e18e004075add48ba2f5dbc56227e`  
		Last Modified: Sat, 17 Aug 2024 08:17:26 GMT  
		Size: 320.9 KB (320926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3384e5dafac4b0036f2938b31928d2a6c84c3a48e1ba507b8195aad8fef530c2`  
		Last Modified: Sat, 17 Aug 2024 08:17:26 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb68967ebabd78c4007a3525fdf9e9e2aeee49ce8d648cba58b90d3e0e37995`  
		Last Modified: Sat, 17 Aug 2024 08:17:27 GMT  
		Size: 26.7 MB (26667225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:96ef24af912a82ae6a1b8f5d2f30b7309befa9fe55c2befd558d62a80103c773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23868618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeec9f565a03b1093f73b2ca48286aa277db15b39c86fec62ba06b3a103d452`

```dockerfile
```

-	Layers:
	-	`sha256:ad2e5c84a6134bd53a5caeffaa58c4a747824754885ac1c5879a800648d35f58`  
		Last Modified: Sat, 17 Aug 2024 08:17:27 GMT  
		Size: 23.9 MB (23851106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d5f6f34ffb4a74959b8e4774119d5a737ee02015834fc53c069cf7c89c85d8`  
		Last Modified: Sat, 17 Aug 2024 08:17:26 GMT  
		Size: 17.5 KB (17512 bytes)  
		MIME: application/vnd.in-toto+json
