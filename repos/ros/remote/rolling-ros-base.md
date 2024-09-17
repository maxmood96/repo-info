## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:b01cd7e9d50e94f7cc49c21f678c44eee57f33bfa65c08ec47aeaa3e6671c3cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:996f92c60bd09b8f53044c7fde439f7dd29198a00e636729def7e62b6d657701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301021444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a45f4801129516dcf117676228e2bd5cdb416b1380da6ad4412c17bee974d`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b605a96dad984d6f6d44736e0781fb44f40a42494c61f4b592540d4d0533c`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 114.1 MB (114118324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f77a16200a9735ad4fd69fa08adb5a87c0ceaed92fd225ffc2613ee2e0d57c1`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f95d60fb7276439314b252ed9be57377912f470fd4ae76fcfebabc4bd7826e`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f98cab3b6517823eae319e8222596dcfd4850d36c0cdbb808b8814a387f25`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 27.5 MB (27526899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:cdef78d2e495b1a5b1effe6edd88fb43dfddb84ec7c05d7c467fc2326f9bfe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23862654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c07a57643b1a96636f7735179c1021db273e77fcb0bbae2af07e6d01f03773`

```dockerfile
```

-	Layers:
	-	`sha256:3ab282fd77006fa12654f991c36ba36c81b332e2fe4dbc54e3dadf4bf73ef9e2`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 23.8 MB (23845515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87648a82909dfd121e60111879464d3f2a7babd73943151464defeed4f8395fb`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d71c39cb6b63156baffdb7a5b8d45912751d5f5ace4928d2b9a55363f23bba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290754161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b36aa65569365a24aa1f971f13125c60fa7b0dcd65486a6f8172de3a62fb4d4`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3a3e4a34e633e0ae3ecc340c7da0f9f3e82dfd31ca88b883cb9f8981cee21`  
		Last Modified: Tue, 17 Sep 2024 06:18:16 GMT  
		Size: 111.0 MB (110959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68216777387a38d479338b542d4ee354502e97cb5dc91de386b7484105b32d50`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b477f8bac49ad74bd4d971d0df8e3b83a3fa71d5285c1549d2457d638a18`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689cc2dc2897eeb8b429ed9b70b4d02255aad2640d936450a544d1fa3849c714`  
		Last Modified: Tue, 17 Sep 2024 06:18:14 GMT  
		Size: 26.7 MB (26666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b20dfc6ab55d2f07f4abb3e397eb573a0325537044898cc11391e4ef1dabff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23885700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbab634007531fbe64697dfbefda0e300b6baad6ad9a722e0da9b736ea1d2575`

```dockerfile
```

-	Layers:
	-	`sha256:a2f40ad0a51c075df1e190b5a9675cb8e8c642dc8518a986ff2c855efbd44c33`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 23.9 MB (23868188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25536249a626d79d47197e21de3ed252e6d219fdf5af607cbf73b1f158a92f1e`  
		Last Modified: Tue, 17 Sep 2024 06:18:12 GMT  
		Size: 17.5 KB (17512 bytes)  
		MIME: application/vnd.in-toto+json
