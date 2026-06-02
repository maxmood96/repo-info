## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:6941e63804cfdc1d5f55d9c1e2a50d1884560c36ff7d6bb63b60b31d8bb6c9d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e6365a9c309a2ad3a9a0526284c451ebda6cf2db0ce02026ded46a749f7fa83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157334687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b07f782190fef3323a313263244ed1b01efe9dcc8df4ed108a3523b93d0014`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a779e092720bb809b4eb6b2dd010671aeb4602999130aeb57e57a9477e48f3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18499996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05db7422452f9fbcfedbc9609ee146ce64263c4a7f7addb74621635c3c39ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:d9448848711be7fceca4ab0d0e4fcd9f46b2ed9e6b92fdc48cb12b6a652d717b`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 18.5 MB (18485388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2fb01d3c44498276833fc9676c638e9b3573b366c86c3c0b4a40a9b43c1c85`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:68f123c831efa2a0368d89d406446092f0f3a8b7a93e4cdcab1a63d55eae58ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151269956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ce9946e8b91b8ca5118b110dfeaeeff25fd0e54d094582ffb08f90c6e6fcf3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6f5faadf10a48aa1dbbb884cc0ada0d1a3a3f12b65f7c71803ae1d42b93a4b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec3f0362ffd357183e1867501a5fc9270c2d12abcf0662ec5f80775b384b047`

```dockerfile
```

-	Layers:
	-	`sha256:79d7be2339d3fd5dc220cef6585bd2209cc4f8d802b007386dba6fdf598a39de`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 18.5 MB (18459394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87f6d1b18eb8730900a9be04dcb6144e701277b1b8bebede669444c5f404b21`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json
