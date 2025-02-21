## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:5af846601cbf4fa3671c0ddf992189cc33ce9164d6e756e0542623efef4f248a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:18f15f3f8432b1be111fb72ebbc410047664b4f680bd7744e6634057abcf3514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157691422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0d4bd6e28d429945958565be6e95e3ff8e96b506bbc107b3d243d73bad465`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4e853e6ef796bb2d217a79ef893c3ad8cb8fe145cac13c5bce5a3583380b7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17833423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258279ca1f78057a4fec6b81d1a3e316064fc445a26ff51a436550f38144c4b2`

```dockerfile
```

-	Layers:
	-	`sha256:9416d105ea50d8bc71eaec30085ce9241512676de54ca8e9b677506aeec54a6b`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 17.8 MB (17817051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11467de67a55ad20db85450e4773d6022a5f7016ce15beeea6ccead6f4dd7275`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76ed25dbbba2ef31a17269383de3b24153901c893afd498dbdc9c44a1ef08a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150730868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9830a0bcdfa4a92fb5779147760eed05ea536e92198dfac321eed067e86c50c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:94beac2dad6b5fdfb4546744fab413618c75f3c0bcadd7d5c321cfdb8d21d604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17807569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b22971271063a3e8b2314420d4e1cc3a9dbabf11185d23b5942be6bdf8acc1`

```dockerfile
```

-	Layers:
	-	`sha256:ef79ca9e0ba93b4fdd14b46b033d82f19706977aafb5296e273ca5441444438f`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 17.8 MB (17791057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7726e5e60767e39d00debef65c31d8d3a4bd7f17648e8885480dabc72e8d91`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
