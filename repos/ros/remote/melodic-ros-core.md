## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:eac9b9f3bf020af5101838ff7a9b18c84855d8ecc2ea79a4f88a2024c7a1cef7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0d068cf63ad02418e9f5b13e2bb2825f99c8b494f3df3f777cc0e2ab7bd4e52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290806827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb13b516b0b4e9fc80366c84fd4e6dc691f0471899f313e6fb928703aaeab95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=melodic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
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

### `ros:melodic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:0a10404d0b3e433a81a5dbf1b344368e8c1f459f755bc1d8b8656c4f68f77c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27043138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79504bac218c7e7d0a736f8a91fda75fa744d6da9583a7366b879b8daf171812`

```dockerfile
```

-	Layers:
	-	`sha256:a9fd9d2f5751ea65b09105a005e8873e06dff471e9861d10a4f297bb7cf6e894`  
		Last Modified: Sat, 07 Jun 2025 01:24:21 GMT  
		Size: 27.0 MB (27027980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d435520d14a39f8fac8d22d58856fe385138a390c4e5f10b2bdc4a9ee1fc68`  
		Last Modified: Sat, 07 Jun 2025 01:24:22 GMT  
		Size: 15.2 KB (15158 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:a36139dbeab7832731584add871cc6d595030221822a79c96dd1054fdd36d7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265185001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2a5a99e27353b069a876ba837c8a8fd866afeeefc09ad2bab3a650a26ff458`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=melodic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
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
		Last Modified: Fri, 06 Jun 2025 23:09:44 GMT  
		Size: 239.1 MB (239062523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e39d39eb235295d2196782cc646b9ef557b3ba88422dafc2c24f46e404a86f`  
		Last Modified: Fri, 06 Jun 2025 23:10:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:7a7ff4aa06f95a41095105d2e602c137a728646921f78ab7db059c2255d5bd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26815409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30334f1ca2704ab4a90d22872a43e9d1454305f73aa94de9259e1b1ae80fb225`

```dockerfile
```

-	Layers:
	-	`sha256:008de32938f1ddc5c0465256c53a55362fe7500e15b9c4988a00673e7c691b6d`  
		Last Modified: Sat, 07 Jun 2025 01:24:48 GMT  
		Size: 26.8 MB (26800145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8871690770d7a77f9bc34c0f59108c64260fb25e16f4301d79a1f1c504ab54bc`  
		Last Modified: Sat, 07 Jun 2025 01:24:49 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2b5fa0341b40e8e2837c4bfa69f04a8ade0361e570d58bb026b979a0a7180cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280321483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fe80cdb993ae116aafb84a2d463b7b249ce2a42063e7b519d44ad57858e1d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=melodic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
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
		Last Modified: Fri, 06 Jun 2025 22:58:50 GMT  
		Size: 252.5 MB (252515945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438816571a02eb55bcd5dbb3be5f0ba77dc9de831c38695c74ad4fac70fbca9`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:melodic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:55f2b7db2d7ffbd7ee92e5b7d9f5ff161731e7021b458dd1a2b10311be3807e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27016067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120bcc152fda13d99874256e6356fb4f88480744cc6077caae18f08ae90127e5`

```dockerfile
```

-	Layers:
	-	`sha256:7e5d315a9b990d027c4d07884075877e14f3a8ac93bd422da4952a0bf39bc547`  
		Last Modified: Sat, 07 Jun 2025 01:25:14 GMT  
		Size: 27.0 MB (27000775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fdd87b7022da7326736be2077aca8ec7fd0336953194fd34b57ef1b85c7054`  
		Last Modified: Sat, 07 Jun 2025 01:25:15 GMT  
		Size: 15.3 KB (15292 bytes)  
		MIME: application/vnd.in-toto+json
