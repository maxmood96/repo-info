## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:1a2db86abbc5f245886bb84ede59f5ec82c078ed77b36b64ff53f42a44482718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:a5c9c39ff8992e17f87b2dfa7ce09ae642044071dde7d5a9a7bbb602b78d6682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142685785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129e2c3b2e371aec1997ff5be0e72246d4e7d161ad7f1815a31fbac329a1b3d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:18:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:18:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:18:49 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:31 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:19:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:19:31 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Mar 2026 02:19:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:19:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:19:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd2c34a991a09624371b32b6fcf6e92986a8301e422f6a558b4e8f4f18329a`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 1.2 MB (1213999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b63153c9a2ebb39e2467cf3e67d0cdf495bd07a8890b0f80e6d844df6cb0fce`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 6.0 MB (5994245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2aa55869bdf08d5e26fbd25963cad70c5139100319ef54869a9d35af58a886`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 97.1 KB (97096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c3d498b896bd0d680b2966d17c9d2a0a912ba15945ea1193c3a3043d7908b`  
		Last Modified: Tue, 17 Mar 2026 02:20:02 GMT  
		Size: 105.8 MB (105841728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c68a8c01cb6477e1a800c4558943962ec4f2c0d391d4ec763c020fa40e39af`  
		Last Modified: Tue, 17 Mar 2026 02:20:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:2830b62d905b671024b308c8d6da80a24bed40cda79ad3de42d429e3a4ed11ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17701204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4e856544c0df146f5f645076943825ffa9b79bab88b6fe1e57c3505f8ea942`

```dockerfile
```

-	Layers:
	-	`sha256:90f143e6e55b173e84451e014a226ce79af03dbb562a09a1bbe7fd9e79f3b1f3`  
		Last Modified: Tue, 17 Mar 2026 02:20:00 GMT  
		Size: 17.7 MB (17686590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:643982524e2ea18b967adc7dc8034e421a98e526d83f4b60823285701e7e7477`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4472ac6b3dffc1621b33f47e6d91945a8d2571cdcd112048cb5b8d10dd88bc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138224966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7487ef09ea2202ee7139dabbce7f965731ef448469d3927e5a18b8a51502986`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:04 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:24:50 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:24:50 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Mar 2026 02:24:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:24:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:24:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08eef9390c8d17a2867d2cc67d4ec838c93c03a7045dadcdeb0e9bd339e8db`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 1.2 MB (1214207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baacc168eca73410a17a8b087d985e0d659de747ff5e3f5a00d5b462df941040`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 5.9 MB (5948658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcd5bd5f34de5076585c79ef1dd14ccdbd39f658cee916aeebde11ee7e95f65`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 97.3 KB (97256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732d4ac40268f48126bab964c6e31a9ac6eeec5a94ed0c805ad4c2b81a4c7c7`  
		Last Modified: Tue, 17 Mar 2026 02:25:19 GMT  
		Size: 103.6 MB (103575625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd97b542b267c300e8a50b87930c719a06c2db81cbf6d6d2246ee634fa990ff`  
		Last Modified: Tue, 17 Mar 2026 02:25:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f4e39043dd3340cc0bba10e3399d47bba314fb79420f5cf5fa8e88a4e06d3712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17687674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f702d9896dc33092423873341d41fde30d8ac4755cdbc465180bd149290cd3`

```dockerfile
```

-	Layers:
	-	`sha256:72e3f567437c7b7cca1dea639dbbdf0d4c612d2c9f3889ed4c8c84da9ad24de4`  
		Last Modified: Tue, 17 Mar 2026 02:25:17 GMT  
		Size: 17.7 MB (17672935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb65f61e8fdabae79302f8d041fd000e91f1bfdaa5adbf72feede01c99d9f0e`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json
