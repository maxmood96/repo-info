## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:a4ecafee1982b9de405f4f939a55256ea3d6516f1bfd155b3083b2df4c827a48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b5c6ae3c2af0b27c7aa45670a2e1420470f0418c9e8d64ec6b6bbfd832a76c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.4 MB (954410616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd76c60238277341f88abc5d4159446cbf37ec47bc7740831f3eec7279db66b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc0cb75a96fc365033e9c90cb0697634a996ee830f32708e403456ed01f4d52`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 1.2 MB (1214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b4e896071636d3437de6efb01a5545c16484eb75b086d3d310b105c98a95`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 3.6 MB (3625685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3e7277c8168821d69668561f0684a23df95676641b2f5bd5939191de98b0dd`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172492cea75e76031d73eebab577b7807873b0ab5dd42540f0472724085f12fc`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c0dd50fef2133f73e56fb7b321bd941e63e5126799a68a6c46d7639ae32857`  
		Last Modified: Thu, 08 May 2025 17:04:51 GMT  
		Size: 106.6 MB (106624981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c48063d83a7c29eb89d52e692df6949bd3682caf3db40bec20778eff8176e`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e893907ceaa195a693dedfd545a53935733a67350077cc004aa4f25023430fb2`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 98.0 MB (97953904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021f2e34f666bc8664cff4806c8662a806201edef9ff624154ba152b0ada1c5`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137b6ba43f0df1ad8e21f42cb7c57d4412b897e0c6d7b5fdd3e9a4dcfc42075`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed447533d41473355fd6a2e0e7ae69b04a36d09b4960da437d919c2de5ae2cb`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 23.3 MB (23292617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa45741a6fe5c31fa8691242237a44ae6da770ead56dd350f5f0a018787601d`  
		Last Modified: Thu, 08 May 2025 17:26:54 GMT  
		Size: 691.8 MB (691802765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:bbd2a3b42fbd5bcaf3a45854ffa585e714e216168f17508140c3b7283ae7bdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57563900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a2e3b14a443b483b7d1166b217c47f5c9235db5f2c57a0b7ccd5adbdad05f1`

```dockerfile
```

-	Layers:
	-	`sha256:4ac995e5d911a60994aa7c8f4b290e2ada10db641fe19a9dfff97856d5b0e492`  
		Last Modified: Mon, 05 May 2025 17:14:42 GMT  
		Size: 57.6 MB (57554200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c51f88eceee775201390ddf4b8692e4560a34f53fd6e179f2d71b67fe2db8dd`  
		Last Modified: Mon, 05 May 2025 17:14:41 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c860d87ba4a91c13a8901111668c04dccc2e15e97304abffc8831e331299de65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.8 MB (914759790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18651555eb718f49ada57dfdf282be131eff019510b814c89687b33f0b713d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cb9a0294d009c4eec5e2391695508957ffd90e81b450a700f767c52901c08ad9`  
		Last Modified: Thu, 08 May 2025 17:16:28 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd089382020f22def49e855c20fac44da7eaab36afaa0b76401347b835355984`  
		Last Modified: Thu, 08 May 2025 17:16:29 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf397c31a610cf57b769f67d08246772afbc66e9f315fe040521f76cac6d0c6`  
		Last Modified: Thu, 08 May 2025 17:17:20 GMT  
		Size: 104.3 MB (104332265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf71f77027436cf6bba595cb99831adbc751cb050909152fe688b4d5925e9d8a`  
		Last Modified: Thu, 08 May 2025 17:16:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9971dd4b19b510a2f1a71bafbc53170c446bf06ed71ebef714bbb5a905ad5e3f`  
		Last Modified: Thu, 08 May 2025 17:16:39 GMT  
		Size: 95.5 MB (95505714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f3d829f2919e9b050501cd51e467f893aaf8f0aa9bf6b034386ca901643245`  
		Last Modified: Thu, 08 May 2025 17:16:25 GMT  
		Size: 360.2 KB (360163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f517a73c8451d9a0acd02357f5bae55b878e2af322a55c7605fd57b82b898913`  
		Last Modified: Thu, 08 May 2025 17:16:26 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840fdee41f175024f1c811c9ab1438f29f706a096bff80e6a1db1540ab3bc87e`  
		Last Modified: Thu, 08 May 2025 17:16:27 GMT  
		Size: 22.7 MB (22680578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694f6ca075e9f2f4084a8457bdbcc24a123b24e7e2343561daea83a7d53f5cb`  
		Last Modified: Thu, 08 May 2025 18:49:09 GMT  
		Size: 659.7 MB (659711015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:df612de684dcd26a57fd01cbe13b16e240c13dba47e7578143d6509b7a4ff4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57559817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a465b953efc949a10d86ca568f297edd092dcc22f65d9418e1a9fedf21456ade`

```dockerfile
```

-	Layers:
	-	`sha256:6b93a752d0d1817f3a3df811a6300d8f48a1daa3b10cd5b9218abe315a2b25df`  
		Last Modified: Tue, 06 May 2025 01:22:48 GMT  
		Size: 57.6 MB (57550036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f36f272f04817074ab5bf730989262fd64e49ff249c6d075a5ebe8ec4ab77b5`  
		Last Modified: Tue, 06 May 2025 01:22:46 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json
