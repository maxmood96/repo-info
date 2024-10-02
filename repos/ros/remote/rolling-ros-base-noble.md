## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:506a66416aebff7ab2babddd6b60e7654551894f8f3664b08e16c8c439d17077
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:31bc36ba8cf8c9d707c7438c9f078ddd2d86d25494f7d266a7299abdd11341b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298624820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965791f5dfc2b96ccdd80d51cdc11e9d5764dba7e5e862fe219525a9a8f17c87`
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
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
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
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7a0c929b90cdbc59c51945e7048addf96d4fe1d056ad03de7f50c53bb3275`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 683.2 KB (683225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b0f84be38266082bf39a65eae2b9ae257266538a89b63f65b773de70a7c94b`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 3.6 MB (3559541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e31627e129edf96cf1d8aa1bdf1803ddcdc1a44632e3dd98212ffec7cee145`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5291007b05b8be4b8b7643e6cd088c9e7a07314b8a45b92ec82c09dedb18dc8a`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3ed0d059c56b7593399c6cb939d4a2c6032bad2a62c73e1901490d5dec794`  
		Last Modified: Wed, 02 Oct 2024 01:59:17 GMT  
		Size: 122.6 MB (122642555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabf54d65021ba841e554915353f0eab36fe9e3dc62cd759a0a8f8221053badd`  
		Last Modified: Wed, 02 Oct 2024 01:59:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6c38e15c192672b68d75d6192383f7a919d5d1ff90b8ed1771807316a162b1`  
		Last Modified: Wed, 02 Oct 2024 03:00:13 GMT  
		Size: 114.1 MB (114130061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ef0b3b2aab6184add5a51f40b423ef6a6fa44966f0e1cfa3b6f72177ac68e`  
		Last Modified: Wed, 02 Oct 2024 03:00:10 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83652cd031f602624bcae5cc022fb8e4769e6c2fbfe21a43be230559644a5391`  
		Last Modified: Wed, 02 Oct 2024 03:00:10 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177231517727644738b63fa94929c8340d19694db793cddf6c44be44f848aa2c`  
		Last Modified: Wed, 02 Oct 2024 03:00:11 GMT  
		Size: 27.5 MB (27532027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1cd0df9ab8bb257f4f219c1b3d16089e0966d5cfa7fdb0ef196d5d16d242f44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf30893c61942e46e94f348a26a36914930f13a2034fbf6374318d6236069b34`

```dockerfile
```

-	Layers:
	-	`sha256:9084baafce384b053940935b2aedc2927069a71ac960e845363a9aa92e974efa`  
		Last Modified: Wed, 02 Oct 2024 03:00:10 GMT  
		Size: 23.8 MB (23848017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df48ac3f0cb573382554309c885b777c2f7a3d9f5fa9762fd48cf3ab9ad3c7a`  
		Last Modified: Wed, 02 Oct 2024 03:00:09 GMT  
		Size: 17.1 KB (17144 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

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

### `ros:rolling-ros-base-noble` - unknown; unknown

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
