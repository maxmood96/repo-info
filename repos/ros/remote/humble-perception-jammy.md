## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:f32f0e38312940f42e1a76ba447b2547719e6a4d0c1a0529563f73ef3d5cbb80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:3c180e282fa904a0c86680d1e23cbd55f3b224056560824ebe914a5c851501a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.6 MB (954626379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bea01095c8d454f0455eb8ff51cff83d31c07818a0bb3ab5e6c1951459a9334`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b938bd7208ed5b0eaf7eefe1ae75db592dc2af1a0dc7f1121d43ea3ef16c1`  
		Last Modified: Tue, 03 Jun 2025 13:32:42 GMT  
		Size: 1.2 MB (1214046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e6b18c4447038135f63984efc97b8842e418685dad2282de87c44c48ce44e`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 3.6 MB (3625823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d771cf9dca927f4be9e036769022665873df4fd6fa780bc8163b714c8c68805`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcad84484813c07387f81500606d7843b0eecb7541913bb03acc91b161c7a39c`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465ddcc433f506333cf3b5c4607f2953f2530a9c3166172cd6c61e26fdd90802`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 106.7 MB (106741362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c69a09fd660cffda2e05b1ab7ba3c202d17a35be834c48c0bb4cb2269494343`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1366c775a6afee125db0240ba46a1b496944d8bffdac140657290439cb7f23`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 98.0 MB (97953334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dde60de9f6eb26f19f6dc5856b7ab5af91825d8d948c17d4721a41c2d011d4`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1691a8c998bd5fbe5b858f792b7c47b5c449d93e878a1e6a3618e8b9b147fc2`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ae0d38eb04d9de1030ad529c255dcadb83988730f005b3afbdfd33e362fd57`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 23.3 MB (23292613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9db296d2aab32b97465a04c98c448bc808e5b46ca8492e0734d1465321144`  
		Last Modified: Tue, 03 Jun 2025 13:39:52 GMT  
		Size: 691.9 MB (691898596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:8fd974c9fe6ef0ca7d3bc3dbcec607b506b09f46c7b4919e3cba5d226f9d9dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57825802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0bead5f0d7f28250aec67549665380e3e32b4603d2cb3fa1f2433a4588d8c6`

```dockerfile
```

-	Layers:
	-	`sha256:2e3daf219a5e5e97682037067aa610035a9fe9ca28edc0e4a4778d4cd6c70522`  
		Last Modified: Tue, 03 Jun 2025 12:11:36 GMT  
		Size: 57.8 MB (57816101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c3f070dd3ef64c0df868a3390036df5a162659e1c71048ec91a192053b8225`  
		Last Modified: Tue, 03 Jun 2025 12:11:35 GMT  
		Size: 9.7 KB (9701 bytes)  
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
