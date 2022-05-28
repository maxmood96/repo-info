## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:9245df098abf2dd563bb817b91dde19c2ab77870e6a3c3b2ec302fd2c200f548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:0605389be2af738b7ff74ca427a0f7dd1dbb156dd520685619a86865904de149
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300499450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410a8af2b677c184bc09c280124717b2d2bf4680fa73097e88962056cc463c4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:26 GMT
ADD file:54d60144d251caa916ff50606bc2364131d47d6b10ed83d08c81c647ab56cc40 in / 
# Wed, 11 May 2022 01:20:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 16:08:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 16:08:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 11 May 2022 16:08:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 11 May 2022 16:08:27 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 16:08:27 GMT
ENV LC_ALL=C.UTF-8
# Wed, 11 May 2022 16:08:27 GMT
ENV ROS_DISTRO=noetic
# Wed, 11 May 2022 16:09:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 16:09:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 11 May 2022 16:09:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 11 May 2022 16:09:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b03a94565ecb6e02edf716307f25a0ea5090e3e2f7acec6a3687b95415378a30`  
		Last Modified: Wed, 11 May 2022 01:25:33 GMT  
		Size: 50.4 MB (50437966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7806f53f52d18737a208f3d99a352a6a818aca1737f3036e6cdd2558cb8c2878`  
		Last Modified: Wed, 11 May 2022 16:14:00 GMT  
		Size: 10.9 MB (10892016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfabd810e159ce51f93f3439c49a3eb065c9cabccfd2ff19aa1f2e973cbc8f`  
		Last Modified: Wed, 11 May 2022 16:13:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0df902248ee6ae3eff3eaec0243df161bf028617ee930cbf1b96e389230c0bb`  
		Last Modified: Wed, 11 May 2022 16:13:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc9931a4cac56fa18fbdd7e81f03ca32b58b2630f364331ba224eec67fe7e1`  
		Last Modified: Wed, 11 May 2022 16:14:32 GMT  
		Size: 239.2 MB (239167058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef75ff8b7b329e7b59d3dd6d4bd0c62f9f83d1b406614acf18d686120abf3af2`  
		Last Modified: Wed, 11 May 2022 16:13:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa6f900f8bc4964429c7cec97fc45e7755e94ab2b16b7e4dc1ade8d90af5ebd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244293952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09146ff9c87a825048dba6a2047746045307900a5641c45537539fc17dc3280a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:31:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:31:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 May 2022 09:31:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 May 2022 09:31:49 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 09:31:50 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 May 2022 09:31:51 GMT
ENV ROS_DISTRO=noetic
# Sat, 28 May 2022 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:33:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 May 2022 09:33:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 May 2022 09:33:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3038e2c6f4de92209486b85dbcdfb0c3794568ec22f4fd2438f984045c9ab600`  
		Last Modified: Sat, 28 May 2022 09:40:41 GMT  
		Size: 10.7 MB (10688315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3e60f35c740bab355e4948391f92c4a13422a4e4c8b87db723eadc9c13293d`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986db8ad07690449985043b0f62b086ffb7575f69651d238a6c7914d8964a16a`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5687faf58ed162f39e6695b07560ab17b035ad665611906636878c34709ce634`  
		Last Modified: Sat, 28 May 2022 09:41:11 GMT  
		Size: 184.4 MB (184374214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a862c7e717410bf0c285d49d4b7c55f6aa21daeaf531c763e01ba890bd544d`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
