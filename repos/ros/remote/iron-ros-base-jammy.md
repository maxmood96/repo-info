## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:7c24479d9b463d0c5cc0fa7a69634a90e53081cee5becdbf81e2be49d46e5e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:8c6e8a540e4140943df22f2623af6dcf2982c436a52e69c43408dad8564ca0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267764406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e14e6177e1a1f47c781db8e558eb54f6f6208d8a1bf0a6fc71fe52357a47b94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b7ba1b6807258e18f3a610bcaa7253d6168c5c2c9b59ba2c7a876b9d847a1198`  
		Last Modified: Thu, 08 May 2025 18:08:07 GMT  
		Size: 85.0 MB (84979096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa6d6a283057ed329e2de93527c1978793816734e6e9525396b835613166987`  
		Last Modified: Thu, 08 May 2025 18:07:42 GMT  
		Size: 327.7 KB (327663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2150dcff14334c93ff6e336555ce1b583b6bd65a0af69e64e0452baa72b6b1c9`  
		Last Modified: Thu, 08 May 2025 18:07:43 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e332ca523c855f708f6ad9ae316e85293ec5091f723e75d9191ba8fddc4ca`  
		Last Modified: Thu, 08 May 2025 18:07:48 GMT  
		Size: 23.7 MB (23734869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:a4cfbbc141a1ee5619df03a14c9c72d0bd5050a186d9aa6b5e287dc53a77cd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc129898acf9ca1a8d20b3444af4b572d82fd90c77d64d2c14623d7ad695a08c`

```dockerfile
```

-	Layers:
	-	`sha256:059084cd6767658e9c4a9407baf00037c06e9513febf7d587d68d1567fc627e2`  
		Last Modified: Mon, 05 May 2025 17:05:24 GMT  
		Size: 23.7 MB (23721176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5bd04864ecc4de40a2d7345e40bf4eedc0a202261a1ee4f32d98a496c3fe28`  
		Last Modified: Mon, 05 May 2025 17:05:23 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4f432727e8d058203c708227549138af90381482c0d01a12f503f4330ca3553a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260081298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1f45ef254089ec03f670aea9f6ee312737b0c6ed871c030f560322441abac2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
		Last Modified: Mon, 05 May 2025 18:18:32 GMT  
		Size: 3.6 KB (3639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922aafdfc15ae9c881fd82e4e3e53df73441681199b1b01db75310e5f0a45d84`  
		Last Modified: Mon, 05 May 2025 18:18:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9cf91867e168e459c65056e05887e6908749dc4d5082fa5add97df0dcc3561`  
		Last Modified: Mon, 05 May 2025 18:18:36 GMT  
		Size: 121.8 MB (121800501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18131159dd922a7314f395fa4055495df138d067d9b0194a8e9e18c53d2460`  
		Last Modified: Mon, 05 May 2025 18:18:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8bb4d88ffdb04c7bb60bd4f9a7691584cf0238fe86687876779447f97afb0`  
		Last Modified: Mon, 05 May 2025 22:48:27 GMT  
		Size: 82.7 MB (82653297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b752753349c66cc54bae91b0ff6c2817b0aa4356ef1b1f12a85b9dc8cf2095a`  
		Last Modified: Mon, 05 May 2025 22:48:25 GMT  
		Size: 328.7 KB (328663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7481703a07ed4e39999fd6961311bf8feaced94bff18d8a3f0c0a353b82ae545`  
		Last Modified: Mon, 05 May 2025 22:48:25 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4b919ac4e10b19850681d4db27a6c63e99919af01e71fe69023235b934c4c`  
		Last Modified: Mon, 05 May 2025 22:48:26 GMT  
		Size: 23.1 MB (23127145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:a51350a1e490ad6c8c444b9c505709f548500cb6d03b2375b187ed2bd2ecf490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23751636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340c2d255b6487fc6a33c32bb1c2668e24bfb327ac690c6e93c4fe7a3062beaf`

```dockerfile
```

-	Layers:
	-	`sha256:5dd8ef2e8143f7c20abd78466769bb589fc7f55fba3cc2804ffc225e5386b574`  
		Last Modified: Mon, 05 May 2025 22:48:25 GMT  
		Size: 23.7 MB (23734375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c551de964011c95a90f17fb3d4ebb04d3638d53104e7a0cbb63530ce681910`  
		Last Modified: Mon, 05 May 2025 22:48:24 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json
