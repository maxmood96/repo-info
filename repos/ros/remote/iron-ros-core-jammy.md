## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:243a1071816b06af5c2119860429c4c89681b527877d20dd32a950815cc2103c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:86e1e41a7112571a94a7335aaf4a99aa8e22df57d2b2c6fc905da6db5a6f03d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158720306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b51becad7371230b182e20c98dc6fe48301e2203702f6956cdca3b6881274`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c1e9168f483a894888f9e9335112e8a1cab2026a8d2b9820b66f16ea5d349`  
		Last Modified: Thu, 08 May 2025 18:06:14 GMT  
		Size: 1.2 MB (1214090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08340e5f5c569b79d3d73740235a505deebd9129b2092978ae98f50633712e3c`  
		Last Modified: Thu, 08 May 2025 18:06:14 GMT  
		Size: 3.6 MB (3625704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb3705b5c9d6db0939620abaf1addf6fc707557d5e304a43ced4f4aaa7ceed6`  
		Last Modified: Thu, 08 May 2025 18:06:14 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db0a32c3f4eddbe9611ed6a6a9cfeeae75bb3ea5d6be9e6208057797e604257`  
		Last Modified: Thu, 08 May 2025 18:06:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca899169bd254152a2faeef1ae003ef5f67b789dcd3d824d203f42a6eeb4a9c`  
		Last Modified: Thu, 08 May 2025 18:06:25 GMT  
		Size: 124.3 MB (124343785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8dd1339a4e357ac978e3b91a0bfbe872b80ba84c685cac468507cb5980f3e9`  
		Last Modified: Thu, 08 May 2025 17:23:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1b196fbbff38b8adb00f16781df832224378b7c9c6378502b6adaf9d61ab58a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19242256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de1bf5d2ae502c75dab81857150867423197eecb9710a69b9d0638eedf1cb50`

```dockerfile
```

-	Layers:
	-	`sha256:25282353ac958e50e90d5a45cec48da09fc479c881b4654505c183339c7a34fa`  
		Last Modified: Mon, 05 May 2025 16:37:15 GMT  
		Size: 19.2 MB (19225851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ffe91fc0090a0269968158f6094a393db2d43bdd147dfdd0f29319f22f3eed`  
		Last Modified: Mon, 05 May 2025 16:37:14 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9ba886986f512faea8309a649c7526995e45f5bce06fec47c71027a536e44a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153969758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97af8c482604018636213f701593bd7e8e1426a91e591b71b3a6c97ae0980cc0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2146e7031324610fc8bbf7b474883917c4f0743612759dced572c0b451ba3f9`  
		Last Modified: Thu, 08 May 2025 17:16:29 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dcc592a7eac1b630f5090e3f04ebdba1f3a7e3c8efee89e7b88091bc398b56`  
		Last Modified: Thu, 08 May 2025 17:16:28 GMT  
		Size: 3.6 MB (3596933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e493107531d32f95fac752d02f6d303c00762d4a6ff8d710cedc2757cdc6c982`  
		Last Modified: Thu, 08 May 2025 21:30:29 GMT  
		Size: 3.6 KB (3639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922aafdfc15ae9c881fd82e4e3e53df73441681199b1b01db75310e5f0a45d84`  
		Last Modified: Thu, 08 May 2025 21:30:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9cf91867e168e459c65056e05887e6908749dc4d5082fa5add97df0dcc3561`  
		Last Modified: Thu, 08 May 2025 21:30:39 GMT  
		Size: 121.8 MB (121800501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18131159dd922a7314f395fa4055495df138d067d9b0194a8e9e18c53d2460`  
		Last Modified: Thu, 08 May 2025 21:30:29 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:be215cf5c06d3c4063accbd17150237634afebd09055bc55868e8006ff63fc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19235271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc3550b8c1e167b23669ee31595acd41c3267bb019ffc6966ab38b9ad12e942`

```dockerfile
```

-	Layers:
	-	`sha256:7da22229964d61b68aedae5f55e812c4f2f6c2a05af5c0f4ac67c636d18c2367`  
		Last Modified: Mon, 05 May 2025 18:18:33 GMT  
		Size: 19.2 MB (19218726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e23546d36ed3a01d5863234ef24c91c10eb1602145cbdf119418b890746de66`  
		Last Modified: Mon, 05 May 2025 18:18:32 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
