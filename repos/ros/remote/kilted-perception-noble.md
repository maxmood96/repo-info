## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:d2e4e3adeb8c04596265b1c47ca324e6d9f356241c82ed651d9fcdfd3d4d04b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:3498c793c85f64a55cc8f05d700dcf94f93bf4d66ad6078896e05caa90cdf018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081946320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340705fdf7e84594d321cbc3a5ddc7801b30516286b0333cb8d6afd9a4cb20f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:58:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d468e65492340372f5a757aaa386b1461ba9890a065702f50f680694f9dd07`  
		Last Modified: Tue, 07 Apr 2026 05:01:26 GMT  
		Size: 784.6 MB (784617748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7f752636ed1fbce072cb76ca5d40e3a36ba12d0904f3ab28891534a4b2a5b9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60936688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c951f7355b085115499dfdf706f9c2829695a3d391fdd05e75e2b0261b2301`

```dockerfile
```

-	Layers:
	-	`sha256:001d4cda1a401c26de87a620397bc0db0f16f7848df1f02687f298bc62f264d1`  
		Last Modified: Tue, 07 Apr 2026 05:01:09 GMT  
		Size: 60.9 MB (60927336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fde1c67c4c20d82d0f51689a37f86e8461cf653045f464fb7cba9fa8051c84`  
		Last Modified: Tue, 07 Apr 2026 05:01:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a677d9d345f1b09ed86dd1b168a5c6387cb24ca35a1740992b10ac90ac0e7069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 MB (984494737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1397af9b711850ae30d67d72aa8cb0b7518ef1fc979d6533a4cb3ddc65f252`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb19de17725a4e4df59958e8f258266cfe3b9cd0f7e2e313bece27ac39c98a7e`  
		Last Modified: Tue, 07 Apr 2026 05:08:06 GMT  
		Size: 698.8 MB (698789138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d349fdaaf5e45caeb9c71f7c0941d9d6e4a9284c8dff1eed7d149ac426dec344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60867289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f6a048b1b0295fda9496a03a3e37613079446c10250a7a11bb2abb4fb6703d`

```dockerfile
```

-	Layers:
	-	`sha256:75a72935f0722f2b1cb2d46fe44a96628293b1ffef7d81de372b41fcb7438010`  
		Last Modified: Tue, 07 Apr 2026 05:07:53 GMT  
		Size: 60.9 MB (60857857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58699756c434346ae0a53510a1936d1cb511dfef56773fc99fd5403c5b28b2bc`  
		Last Modified: Tue, 07 Apr 2026 05:07:50 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
