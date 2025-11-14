## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:f14906d4a3ca82fa13ec7f8c79d237a04f6a14d47b69564f25eac6903d319d91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:4e413449e965df0365d69f8c3d1ba8cfcce7462055b2e9f553946038c8fb889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.3 MB (955267423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59770bcd3cb81de41bcfcb45df3b1cd13f144652a4103b9c8a561013c176d044`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0d0741124ce4b0fb32492f0eb411c68db26f35feb0021f90eb30e7d54f867`  
		Last Modified: Fri, 14 Nov 2025 05:35:32 GMT  
		Size: 692.1 MB (692078563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:beb8f658a1af83eb45d4c219d7a6dddd8461f1e6b5ea407917e43aa8cd78d417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58779844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b398c9069f37afa0b64dea4ee59863980189e9bd72350262c9e4f2856040857`

```dockerfile
```

-	Layers:
	-	`sha256:3c05b9e971b9f7a4606bc635dfdf55c3ac7a74cf9a4f7f7b93590ddc2e8daf03`  
		Last Modified: Fri, 14 Nov 2025 05:17:41 GMT  
		Size: 58.8 MB (58770492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a507faa299531991695a31b8854ae95bdd28604e7ac848e2dde9065c3bedf8f9`  
		Last Modified: Fri, 14 Nov 2025 05:17:43 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec183011cf6e60839ceb21854426cef343bcef506019abed261c30357f959409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.8 MB (915797607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9d2f3550dab7e144828cc7546b305d487aa457c6f459bffdc4c1036ff187f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11e17f04355c02a9eadea3e0924ee22951e0a76af18b90e7a44e2cfada4c52`  
		Last Modified: Fri, 14 Nov 2025 05:31:54 GMT  
		Size: 660.1 MB (660050278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:20b8cc1b1082051f1c1937e4002197a0acdd8ee796f9d9b17dd686ade332e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58764245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215b91a017e92d95162e756c7abc222791ac87f692ccc607510a10866c6f48b`

```dockerfile
```

-	Layers:
	-	`sha256:6e41f5d137270010cee9c967c7b1f18ec19e7de3cbe729d862fed5b6a2859920`  
		Last Modified: Fri, 14 Nov 2025 05:19:30 GMT  
		Size: 58.8 MB (58754813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0b1e8fd8dd6d89eda990d19a48a4735fd6141dee4434e2b642439d6a90f13e`  
		Last Modified: Fri, 14 Nov 2025 05:19:32 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
