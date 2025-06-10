## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:d9e8633978b346c6901503375d9a08903cf408e0a83ce168057e7bb7cc606a5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e8f6fee6cb35893ecabaf63abdd1b6155327c09f5f521ecac2aadaac687caa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169548776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955aec7c4ef106f0ecb39fa03b442317d388cb8910625777d945db8d49092bd9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29647462da8b7248faa562686afd7d3260fe5f9ebcad7199b3fc188188ec2cb6`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 683.8 KB (683831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8cf1676bf842067dd91d4304cd9e00b68f99f9e3fdbb5aaf3bfbd7f42b6bdd`  
		Last Modified: Tue, 10 Jun 2025 17:40:51 GMT  
		Size: 6.7 MB (6745430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2963d62bf807e13e004c105aaff40d7c2b5bf0ec34a98c73b58948b204ebf`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 94.0 KB (94036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086be9840220e0654dbe8ca646f01473644e65977961a84a0d7fd5ef2163ff7c`  
		Last Modified: Tue, 10 Jun 2025 17:43:16 GMT  
		Size: 132.3 MB (132309948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15678d18204d5f60c2a8207755206c234b0e17d078a20bf91a9d36d9cde82f4`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:93911fb041f53521ef54ddf326a9bdd7c8d866ba5a115cf9e10fdbd0796e4d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18307405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a9385b4fb2bad1aed6f6954cfd0a5b71a416f479280c4b104fc1d8a6c3228`

```dockerfile
```

-	Layers:
	-	`sha256:a4329cced913570e8cd67b06c68910802fe2eae575c7a6de26c6b70367d7ce83`  
		Last Modified: Tue, 10 Jun 2025 19:17:49 GMT  
		Size: 18.3 MB (18292741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223339431727abc37c50fe07c4b4395a6919bc8c21a63646678cf4c897216d76`  
		Last Modified: Tue, 10 Jun 2025 19:17:50 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eeb77a1f73957b7606e34051c69f230bc502eb5b31773c46010b492db68337db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163386472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8933135da0a27dc5165727796aa861f89353f404798f6dcec4a30ab70db79bbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46fee428ca8064da8e42ab2a83edde8864b2387c92ad4288a4f0a8f4dea7b0d`  
		Last Modified: Tue, 10 Jun 2025 18:23:31 GMT  
		Size: 127.0 MB (126997135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c56dbcf3bcee78c66e7611653fffffc90f5c02e8a46764509d6a4168c73778`  
		Last Modified: Tue, 10 Jun 2025 18:23:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1c18614374730bd8d774d26401abaa44254b26c53ba7fba30692304e11f83c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18281537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b877b83f05be35c15de376e538c8192f8050046c20d50b2e0b083c64b331cb8b`

```dockerfile
```

-	Layers:
	-	`sha256:cf90e5bd12f51b8e47a9c4def18028ed55f5466048c4296ce7edf1376b35d865`  
		Last Modified: Tue, 10 Jun 2025 19:18:02 GMT  
		Size: 18.3 MB (18266747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075e3267b107e741bb6451a4ceb8e79475caa6119d6c02b4493feb22ec440662`  
		Last Modified: Tue, 10 Jun 2025 19:18:03 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
