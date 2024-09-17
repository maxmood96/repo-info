## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:783ff5fc337e6f74a6e0cb434568eb77176689e4f6fd84e9a790dbffa48a96e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:ad74a2a7dcb1815f9a1018f4ab30ee78f7e2aeb76dcf04d5519c3f8bdf2cc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624867892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebd3bb9e89b8c600cc6b7a5a6fbd07a3ce2cbaeb1c7117813d3fc24b8ca201`
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
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:3f1ad02a528230401a48684b4a948613aeb393e6717ea6544cde85fc9f715aa1`  
		Last Modified: Tue, 17 Sep 2024 03:03:18 GMT  
		Size: 323.8 MB (323846448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e990cc82764b30f37fec9c1f5931330849ae62a65ec5546dfb91ccbeb1c20352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42136334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3a8e22f08fc690434d972d528a92853ba42227adabfe89720fc890aa0ac941`

```dockerfile
```

-	Layers:
	-	`sha256:c57118ff9c9d4471bacbc31ecbb9537c98a0f0a1b7fcf36e4761b4d6e1fa174a`  
		Last Modified: Tue, 17 Sep 2024 03:03:14 GMT  
		Size: 42.1 MB (42126658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9287123322f645739abc85bcb379154409782f1184901d9678934553c4107a6f`  
		Last Modified: Tue, 17 Sep 2024 03:03:13 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f851921a94ea1df27f4f7331ebd28c6514497cd697c08622f0a6036c750e0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.7 MB (567746100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892beca8c7f9b20d171f2b8789d277f9b5c5c06af6708ee29dfeca965c049d7c`
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
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e1a2aaecfd712d989271a79d7d1ce0bd52def4138d984163622896c268187394`  
		Last Modified: Tue, 17 Sep 2024 08:10:19 GMT  
		Size: 277.0 MB (276991939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d13f3dc3ac6d85040565d4b66d7551e34e0ed3b278f27bb26452e6b04d34ba92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42134788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57e84e899b8ef57488aee5812b1e1a86092db7b9ba25a77c7d5994147a96c98`

```dockerfile
```

-	Layers:
	-	`sha256:4342cffcfc95ef3c91f7ad6fb20397f0219a293598b438b0a6faefc0292ceafd`  
		Last Modified: Tue, 17 Sep 2024 08:10:14 GMT  
		Size: 42.1 MB (42124751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c9fa345bf7c5de14c5591e9dbecb063428ce648b7b5cedf5c90820aa43b67f`  
		Last Modified: Tue, 17 Sep 2024 08:10:13 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json
