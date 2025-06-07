## `ros:melodic`

```console
$ docker pull ros@sha256:b4366ca0536e2ad3654ed66fb4475bc43b7a0c15bd8a5be91fd5ac9dfaf935d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:3444627c80c3d5d4179058e5e9254233df2e0a58fa83fc986da96deea1c720a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.4 MB (436357591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbe13bc69f07b0ab80624cfd51ad7272d699b569dcf96088f3cda2e9646b279`
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
LABEL org.opencontainers.image.version=18.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=melodic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Fri, 13 Dec 2024 13:10:33 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd8ed8441cd37839342498b388249635a383eaf297f5499589ce8979f046f6`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 818.8 KB (818769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e353292c049a62293f145477e75bd0c00382394ddb6f1863dde88eb8191ac`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 4.7 MB (4688794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3511b706eea65501cb1eddcc81b69d6eec72816ed849b948d6a022b2c3e01a4b`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 2.4 KB (2365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac95e42614d3975ed1777db2e3b263bd937f1df26b98a808363abe3ca608f7c9`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fede2c0c9099b285d54aba019597a08c769d8605965589cca16c7a03ff6d69e8`  
		Last Modified: Fri, 06 Jun 2025 23:07:33 GMT  
		Size: 259.6 MB (259605197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208bc360693340c0084653cad3e347704144ab9bb29bf9a0d8ab2952fcc7e6a0`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeda130f479297922c12f70a450908bc7cd9645a402a08c4e0901052336dbc1d`  
		Last Modified: Sat, 07 Jun 2025 00:07:54 GMT  
		Size: 70.5 MB (70457476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ced95aca218869b7e1d44cedac302ce09a180f310ca481b947a8613a7fe5d2`  
		Last Modified: Fri, 06 Jun 2025 23:26:00 GMT  
		Size: 314.1 KB (314134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d9ee43bc02665b236bdd296a13c285ebbca9665b14ae078707177eb7a6f53c`  
		Last Modified: Sat, 07 Jun 2025 00:07:53 GMT  
		Size: 74.8 MB (74779154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic` - unknown; unknown

```console
$ docker pull ros@sha256:6e354796b8f9aa3844533538905ffa6ad243d6a3be14cb218205f64471b6e390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35190403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e632f90f6f49f31253c475599aed437bb364e06e4a29cc7297c2f8d520302c`

```dockerfile
```

-	Layers:
	-	`sha256:0ae439d350e7eb9b9c8f09cda26946a606b78ff43417952578cfe28acaba9bde`  
		Last Modified: Sat, 07 Jun 2025 01:23:50 GMT  
		Size: 35.2 MB (35176704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046ee98fba4be5cb1dca55d5f4c080be8cbfd14a2c522f4a48caedf0d5147ef5`  
		Last Modified: Sat, 07 Jun 2025 01:23:52 GMT  
		Size: 13.7 KB (13699 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:76a7067d17f383b486ee8896098b28d3fa0ca0a856a42de06e73bd4bf4166fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.1 MB (385052423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47818b4604b5c41adceb09e05b1cf367abdcb755233fe191c9d45892af21feb`
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
LABEL org.opencontainers.image.version=18.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=melodic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33728956a279755bb5e348de30626ffff0023b589d4fae264c2722ad7c06e207`  
		Last Modified: Fri, 13 Dec 2024 23:12:36 GMT  
		Size: 21.4 MB (21399001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49dc90beb658024e96db38e10eb9d3d5e95151611e5a8b1e4aac7ea6e45313`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 820.1 KB (820137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd276fdf8bc17a3ae89b76a87869626c84e29eb535dbb5b183ac80bae85c02c`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 3.9 MB (3900545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b029d64f9143b80260f4b5b994450da65eef021667391fbce44a5f2aa0f4398`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ae8f613e6050147490df1dd5ae7e53a70a79bb893ba2fc2f0ed2f7a59af03`  
		Last Modified: Fri, 06 Jun 2025 23:10:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5393a6be3185c54c4b2786a21d6b8fbe4951a2723d98e22f3991a71d1b2fcda7`  
		Last Modified: Sat, 07 Jun 2025 11:46:32 GMT  
		Size: 239.1 MB (239062523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e39d39eb235295d2196782cc646b9ef557b3ba88422dafc2c24f46e404a86f`  
		Last Modified: Fri, 06 Jun 2025 23:10:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc4b18c64adb02b89f0eb120a9f81c57773627408e6a22f89cc14d048624249`  
		Last Modified: Sat, 07 Jun 2025 00:40:43 GMT  
		Size: 55.0 MB (55032095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db5cc57e84332b331b53e7c2872f8469688505d5d4c73d5b72bde75a86d95c4`  
		Last Modified: Sat, 07 Jun 2025 00:47:35 GMT  
		Size: 314.3 KB (314251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f2fccc335f17389487ab30e55309211538c820e13957aa5a7c722d21773ab`  
		Last Modified: Sat, 07 Jun 2025 00:40:43 GMT  
		Size: 64.5 MB (64521076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic` - unknown; unknown

```console
$ docker pull ros@sha256:9bbca9dd01905f5ae3dd12024c89f407d73f80a56b3effc062c72ae932863485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34910873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ccc8c071b25f876fb8dea6907cdcc0aad081979049ecca3358d726d315a056`

```dockerfile
```

-	Layers:
	-	`sha256:44fb1c88bfef01fbb0c51314ce72848d0c48ad9d6edd69fa2cfe023f2e9d6155`  
		Last Modified: Sat, 07 Jun 2025 01:24:28 GMT  
		Size: 34.9 MB (34897081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d0a200d7503463f03b82ab590657b5c1ff45d115302cd95f36d3a02894a7f49`  
		Last Modified: Sat, 07 Jun 2025 01:24:29 GMT  
		Size: 13.8 KB (13792 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:85d442cdcc1b530d401b56f5e80aba6582fdc0764e36e72cc5dab6dcf6c5642a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410914206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97016fd16f499d91166d2a0ea55c5c9088d647b7a785abbf540afe5e2f6660c`
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
LABEL org.opencontainers.image.version=18.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=melodic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Fri, 13 Dec 2024 14:46:44 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6559b6c0a95271b577d553166080f5d9965d9e2d2b1732c96a566175205af31f`  
		Last Modified: Fri, 06 Jun 2025 22:59:17 GMT  
		Size: 818.8 KB (818832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99d6787c1aa8369d0f0e3a1051c56c004c0b42816139b09e85d5fed6e44a27`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 4.3 MB (4270397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5c6de79efb0ec1e3e319f9a58fd5e398fcb65ffb3eff75ff9ff1cff87f158`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ba467d11b0f4ca6086ddbb53b2d1aebfed63ef7e81bd065c9eb80a543d9824`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769453b62edefd603faee246bf733ff43690055c751f211241580ef7f7b09f62`  
		Last Modified: Sat, 07 Jun 2025 11:46:38 GMT  
		Size: 252.5 MB (252515945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438816571a02eb55bcd5dbb3be5f0ba77dc9de831c38695c74ad4fac70fbca9`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab471493d9b16da6515b9f30e94de361c4b531bbb76038e4a2578a49bbbe540`  
		Last Modified: Fri, 06 Jun 2025 23:25:07 GMT  
		Size: 63.3 MB (63279747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c83e2923d24eff431587de1874c98d4e255e1bfa72d41873a51d676bf257c9`  
		Last Modified: Fri, 06 Jun 2025 23:25:05 GMT  
		Size: 314.1 KB (314141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24322448908a93ffaa58a566c9f7ac75a2cee29807c2c4976ae63e8d59d938cd`  
		Last Modified: Fri, 06 Jun 2025 23:25:08 GMT  
		Size: 67.0 MB (66998835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic` - unknown; unknown

```console
$ docker pull ros@sha256:bc5e0382ed24607ee263e62c4c083c693e6b3cca5d1becde5ba55e58508cd626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35095698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e725b76d4ada951d5235a45b31d3591c23b6d62c02fa5cebc0de3235a16bada`

```dockerfile
```

-	Layers:
	-	`sha256:3ccbae203770e03f9d75b1f4c8a3f59e2b9f00540abbbf48995dc02a79c956ba`  
		Last Modified: Sat, 07 Jun 2025 01:25:08 GMT  
		Size: 35.1 MB (35081877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f12bb2f28554cef9f054f9b72a61935abec5dd96eac4066cff36072f04123197`  
		Last Modified: Sat, 07 Jun 2025 01:25:10 GMT  
		Size: 13.8 KB (13821 bytes)  
		MIME: application/vnd.in-toto+json
