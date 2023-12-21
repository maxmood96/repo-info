## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:8b9e1535a8f1261a8909303884d6e1ff83b4948fc87309e0d4857bfc240364af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:35e1478042caf5cb8b06313766683156650b2696239b2aed4af1d058088d1b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212304616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23993287d8e415d259fb06760b5786fac422c1007bda14cc144e09b6821bb003`
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

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:ae9e3f788404607dfd2b776cdfbfd2d735a3e23f68d8d9e330c96b9367ff9028
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187939512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73d774a451e6644e2ae773ed8a3cd66e4a777bf69cd58a447faad2442e29ee4`
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

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f77b8ee37b3f85cd593cdad490cc481c0a4f8d48497c542d3e4b0539296d83ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205364465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbf5514dc4ec1feb8e6d3d214acb8b67eb9594bd6226512f76db100305884df`
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
