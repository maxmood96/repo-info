## `ros:melodic-perception`

```console
$ docker pull ros@sha256:3b7f84af20714319a212c825025e2e42da1a4a2c387feed2db5188e8bab57fd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:625b1618891bf4e6c13021758279bcb33678c3335054e876e6b0bd78d21ee047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.8 MB (741835037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90919e6c43974296814811d3a08c2beac8a808332dd1c1afd0036a8330a8b4c7`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:26fa236c28f0fe3ea918835e676c1c711820ed9df5f2b616dd520605b8f04455`  
		Last Modified: Sat, 07 Jun 2025 05:03:47 GMT  
		Size: 305.5 MB (305477446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2bc3e925c7dec7e810c314356830852282177e5ffa81e49623551681dca16f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51243492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b986906f8b37466bcd0a870b872f8291a18b19b002295b19bb3560e5be365fbf`

```dockerfile
```

-	Layers:
	-	`sha256:24392a54705c7c48dc48ceb4f0f38d610f71a6cce2cfbb47d3d3c39f6c272fda`  
		Last Modified: Sat, 07 Jun 2025 01:24:00 GMT  
		Size: 51.2 MB (51234098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c616c139c9bf1e69c4f3adf7ae60fdbeb089d981688a829a4553df6863e6e4b7`  
		Last Modified: Sat, 07 Jun 2025 01:24:01 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:49ba572a3e31199ab5456c0c17062391b54612718e2ad3f984e71f3055e34927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.1 MB (645147729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cd18670dc824f2f0966eea891d6ca88266870b427238928e58fcc55e317fda`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
		Last Modified: Sat, 07 Jun 2025 11:56:57 GMT  
		Size: 55.0 MB (55032095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db5cc57e84332b331b53e7c2872f8469688505d5d4c73d5b72bde75a86d95c4`  
		Last Modified: Sat, 07 Jun 2025 00:47:35 GMT  
		Size: 314.3 KB (314251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f2fccc335f17389487ab30e55309211538c820e13957aa5a7c722d21773ab`  
		Last Modified: Sat, 07 Jun 2025 11:57:09 GMT  
		Size: 64.5 MB (64521076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985f08227a008924c4e2a2f5c2681a16f795805f0c3237e20e83b12c2d10070c`  
		Last Modified: Sat, 07 Jun 2025 11:59:32 GMT  
		Size: 260.1 MB (260095306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:974e3d7347314de3a838c4ac544faecc7040feeeeb822b825d8cffda40d6d46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48446528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc32b34fd491f4b3097f888f29ec5c8f6bf4763c93887471d0f5fd60f4037628`

```dockerfile
```

-	Layers:
	-	`sha256:7d905fb35a36dd6e7837f326d1e9a8d2bf9680542bd05ae002a7bc9bf4557309`  
		Last Modified: Sat, 07 Jun 2025 04:19:45 GMT  
		Size: 48.4 MB (48437075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db79ba13aae58321aa985c3134a1ebe6d74f1f01f7cfcdb4946e50e8643c035`  
		Last Modified: Sat, 07 Jun 2025 04:19:46 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f9faa6637358388f476d362f7f661ff7e98f542376fe424f56a703b282ed4c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.7 MB (702675155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f7a2fd12156cbc4a5a6a28c74fd54b5a032a7096e9514e988361c3282d1869`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:23713c1d50aaa75508b2c8a99c2d6da79b6f8586a4c08017e782fd6d0041d3d1`  
		Last Modified: Sat, 07 Jun 2025 11:59:20 GMT  
		Size: 291.8 MB (291760949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:618d99cdab2f423466e40d115207a3937b9467e060cc2b91b4406204e60341db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51163607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6ac3774cd64b0e6a0b73ba8d3a00c6e5e2dd445a5c3eb28b86f80e434af5d2`

```dockerfile
```

-	Layers:
	-	`sha256:fc64cba5086bf0b50b56c8ad039c4a928ba8fa8a7148f1abd17fb0ff24bda007`  
		Last Modified: Sat, 07 Jun 2025 01:25:11 GMT  
		Size: 51.2 MB (51154133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae1e92f7e54ddc2dfaa07341b1f5ee787ddefee3975f8405d4c6dc008cd4d91e`  
		Last Modified: Sat, 07 Jun 2025 01:25:13 GMT  
		Size: 9.5 KB (9474 bytes)  
		MIME: application/vnd.in-toto+json
