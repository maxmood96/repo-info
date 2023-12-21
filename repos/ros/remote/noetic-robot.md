## `ros:noetic-robot`

```console
$ docker pull ros@sha256:bd4a5091d870995dbed43a45ff04aec6de76baef6417e8f87d6ce0567cff9b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:bc84d140544727f5d32ef42093623e6960cacdbdb2def4d0a910c082ca439056
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359042741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9548a8e6edb30c384685387fd0e0ea36c88d55a19e1a09f3f4668ce1a83855`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:35:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:35:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:29:57 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 21 Dec 2023 00:29:57 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Dec 2023 00:29:57 GMT
ENV LANG=C.UTF-8
# Thu, 21 Dec 2023 00:29:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Dec 2023 00:29:57 GMT
ENV ROS_DISTRO=noetic
# Thu, 21 Dec 2023 00:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:31:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 21 Dec 2023 00:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:31:21 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:31:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:32:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:32:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0425e951c42dd00ccb058ef6938f79b69db58bf09271ae9462bd5852cfd1353c`  
		Last Modified: Sat, 16 Dec 2023 10:05:10 GMT  
		Size: 1.2 MB (1198846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42aba2266c05b2025e53b1daad133978c157924dd56b92b27baac4c2b131ac49`  
		Last Modified: Sat, 16 Dec 2023 10:05:08 GMT  
		Size: 5.6 MB (5553944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426271c4077fc8907db7081f0fcd64415cacf76ea3b9cef6da9802d28d8d8c3e`  
		Last Modified: Thu, 21 Dec 2023 00:56:34 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf02b27550a0cedd5debe9f2b36d9f259521bcdaa89ef551aeeacda8c5a90433`  
		Last Modified: Thu, 21 Dec 2023 00:56:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cc878260e3acd4bcc306085f3f27a5e84abaf0365e699763d3b4ae390b74a4`  
		Last Modified: Thu, 21 Dec 2023 00:57:02 GMT  
		Size: 177.0 MB (176965314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff966011c3ffea2df45146e8fd785d3847e83574f24faeda0b79b6c2fc731ee9`  
		Last Modified: Thu, 21 Dec 2023 00:56:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b45613285b087c73ae74e7aca39e03b21b9973ce2bcdb9c858073f054b8a62`  
		Last Modified: Thu, 21 Dec 2023 00:57:18 GMT  
		Size: 50.9 MB (50941192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bda7e41343135a259fc3006f9312a1734db249216ad2600f12268b377c615`  
		Last Modified: Thu, 21 Dec 2023 00:57:10 GMT  
		Size: 311.5 KB (311507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae693a9d21da1495dadaaddfb1a279ef525ebbae11b8ecfedac09e9b55ff7762`  
		Last Modified: Thu, 21 Dec 2023 00:57:22 GMT  
		Size: 79.6 MB (79619989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adafb1cc9b244b1bc6840ed2bb20fcba203f481d57662a1cc6c7d754e122d9b`  
		Last Modified: Thu, 21 Dec 2023 00:57:35 GMT  
		Size: 15.9 MB (15865437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:267350a59560c547ebea7d74050eb8c5f6d8cdad7fed99da2e0a2eea9762f5e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303324263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b75ab6037754e5456a8a35a08839d18a2b094e84acf42b345aefa555fea60d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:37:05 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:37:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:37:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:37:06 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:37:14 GMT
ADD file:195375389d64193c828c6d3f379c7e35ea85256eb1c51d2bfeab73432ea46064 in / 
# Wed, 13 Dec 2023 10:37:15 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:37:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:37:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:07:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 21 Dec 2023 00:07:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Dec 2023 00:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 21 Dec 2023 00:07:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Dec 2023 00:07:36 GMT
ENV ROS_DISTRO=noetic
# Thu, 21 Dec 2023 00:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:10:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 21 Dec 2023 00:10:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:10:53 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:11:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:11:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:13:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:14:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba68304511cfd178c72d64196a05b1343fbdbed6093d7b4db0c0d223510c40ab`  
		Last Modified: Sat, 16 Dec 2023 09:27:50 GMT  
		Size: 24.6 MB (24600972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5373ad55d8e8c0ab26bca9b592d8809358e69e59cff53121bcdd908a9f9639c`  
		Last Modified: Sat, 16 Dec 2023 09:50:09 GMT  
		Size: 1.2 MB (1199062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b246e660d5421dff1c723cfa2d5dfaa9c2ccfe1976b8fce4d4d1fedc8f5`  
		Last Modified: Sat, 16 Dec 2023 09:50:07 GMT  
		Size: 4.7 MB (4679510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86b68362247e6c335b1b994e353be4caabbb460dff2258ee39d1e46f0a26b96`  
		Last Modified: Thu, 21 Dec 2023 00:22:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d73e0dc1bcc38ab8b8f185ae82089fad34d209dc6ae684c177004698c31eade`  
		Last Modified: Thu, 21 Dec 2023 00:22:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b004039e385c7bb110e0d7b5d56c74c11d4335f641f6ac820077b7dba5e657d`  
		Last Modified: Thu, 21 Dec 2023 00:22:43 GMT  
		Size: 157.5 MB (157457475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db88fb9951c23e56d318cca2ea94d406b8f3948e4af7f625f5be359c599fe2fb`  
		Last Modified: Thu, 21 Dec 2023 00:22:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5093cb684949f593605dfac2d8a37f1cb033b57b546018f40858897b691380`  
		Last Modified: Thu, 21 Dec 2023 00:22:58 GMT  
		Size: 40.5 MB (40503740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b482fbadb6eb5cc9227f0519baa1eb271de8a275e3e2bd6f7f8c53b0aab442c2`  
		Last Modified: Thu, 21 Dec 2023 00:22:53 GMT  
		Size: 311.5 KB (311511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756355e2b617cf4b1fadfb831ed32661447f1084b144d2cda89a927328376302`  
		Last Modified: Thu, 21 Dec 2023 00:23:03 GMT  
		Size: 60.5 MB (60500263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043b970796765d4abed444bf7ea5015d3325efc964bc7a0250ccc9af3c034607`  
		Last Modified: Thu, 21 Dec 2023 00:23:17 GMT  
		Size: 14.1 MB (14069237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d8698b11180f62ca6092e8bbebbebe7143854d1cc2aaa545ad29c27f4fd14c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338315443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af8e9a9ea09db58184cd25f1e4230f1c992bef44db74cc8b53735b934382771`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:05:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:05:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:06:12 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 21 Dec 2023 00:06:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Dec 2023 00:06:13 GMT
ENV LANG=C.UTF-8
# Thu, 21 Dec 2023 00:06:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Dec 2023 00:06:13 GMT
ENV ROS_DISTRO=noetic
# Thu, 21 Dec 2023 00:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:09:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 21 Dec 2023 00:09:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:09:11 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:09:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:09:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:11:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:12:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3055ab3450adf267aaa7449c6ffccfda8d80fe8870d76661cd5a7a1a979091`  
		Last Modified: Sat, 16 Dec 2023 11:36:49 GMT  
		Size: 1.2 MB (1198805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1234d731199ddd7a60d617e9518f9d1a2a27906869acddfce95b4038e2fde55`  
		Last Modified: Sat, 16 Dec 2023 11:36:48 GMT  
		Size: 5.5 MB (5532123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2924072ea8eb263d250482fa38bc290cfe99727fb4a9ed42281c282f668d8f5e`  
		Last Modified: Thu, 21 Dec 2023 00:41:21 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c838fa71a9efdeb3ec5171520baf8471e181b179adef293f7a30269bc91a50`  
		Last Modified: Thu, 21 Dec 2023 00:41:21 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7dfdc57b641fb12daad9732640a9d7ed176d7b85d7c3ecf7275a2d6d5f1b06`  
		Last Modified: Thu, 21 Dec 2023 00:41:56 GMT  
		Size: 171.4 MB (171427905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e986a2b771d05ef12a5e524eb2454a8e4adbebbca6a4ad7d1aebc92f3c813f1e`  
		Last Modified: Thu, 21 Dec 2023 00:41:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c0afeeda3d8369b29dc81acc7772dc6f53f31c6ae62747a766fffa1003facf`  
		Last Modified: Thu, 21 Dec 2023 00:42:11 GMT  
		Size: 45.2 MB (45206712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1d46cfed634e5d507651b5d1e1dcac6d08b432452f13184d3fdff28fb0564d`  
		Last Modified: Thu, 21 Dec 2023 00:42:07 GMT  
		Size: 311.5 KB (311509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874f9124354c51fd3a1857a4abc35efa5620b6141a48f59981370d6f1f229f50`  
		Last Modified: Thu, 21 Dec 2023 00:42:15 GMT  
		Size: 72.0 MB (71973131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33eb7e316fb9ad7937994715fbd977025b1baf558c4ca005b7fa8d15e006dd80`  
		Last Modified: Thu, 21 Dec 2023 00:42:29 GMT  
		Size: 15.5 MB (15459626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
