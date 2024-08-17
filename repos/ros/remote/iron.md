## `ros:iron`

```console
$ docker pull ros@sha256:4a1f50f322f643639664254d99c51c7df99caaf96b1271ce907e32b61b09ce17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:379242c95e2fc0df3ff873e7dc4cb8f3897aa799c34c4f898da31e870d9aebbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267704187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f697ea9cc5a8853a2279d11acebefd2130b382f4a00a29042021cfacc84e9`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:b6287828e4497dec4d781c2674ba9e55f149423ae252f89c62bb84b1706d19a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075206c2478e07f068d4501dbe416605a5c9910f3d68a5f8c4f7095de507a623`

```dockerfile
```

-	Layers:
	-	`sha256:9c8044a86c7e1b23b681096d75a5090eca18d054c46acf0ba095dc28e8c7262d`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 23.7 MB (23676936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2e2da58e9c10f8f9463fdd00b53f5cc33acab8e115a3d6583dc25f70163896`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:818a23706d437f24e926d2566cc138e2e3f3092fbd069462f6c38f41b3f718e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260032567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a807f2161af5b975c486b48a9835ef0fea81aca1e98dbc96df7c600927473033`
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
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e846c275a2224773f856f9b21a28de97bec6dda077693b87dcaf52e96edc19`  
		Last Modified: Sat, 17 Aug 2024 03:58:43 GMT  
		Size: 121.8 MB (121780925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e2c8c4e647f8d82c8763714a4bf637af13f75885d5e363efcc3f2ebbbe7110`  
		Last Modified: Sat, 17 Aug 2024 03:58:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944cdacda70117eeda69e2de304cc3db7f5fa0301282c8ba23af134f6779e358`  
		Last Modified: Sat, 17 Aug 2024 08:12:57 GMT  
		Size: 82.6 MB (82644949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d887cf2c24dfbd3eabf2b846bece5bac5be53db3f7065e45486cd474eae94ee`  
		Last Modified: Sat, 17 Aug 2024 08:12:55 GMT  
		Size: 314.3 KB (314275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055dc550fa8933849894f99a31ddaa9e3eb3ea86bc4ca0699e91cdff40b716f0`  
		Last Modified: Sat, 17 Aug 2024 08:12:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cb81767de20213bdace44b72d29a09626e510360ff7e6ba3cb6dcb68261e22`  
		Last Modified: Sat, 17 Aug 2024 08:12:56 GMT  
		Size: 23.1 MB (23117846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:ed4a0b1ffea32683d40c720a0adb94b1b40cc8f1b89a091dbc841db787fb5d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23707609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d9de9a00393fd5d7d940feb0a3e67944bd25432f98d4ebbd3ade62d32c4118`

```dockerfile
```

-	Layers:
	-	`sha256:b83963f7a9f555d91581df8eedf9703fb305b66da46d6409d0835fcc58dcad6d`  
		Last Modified: Sat, 17 Aug 2024 08:12:55 GMT  
		Size: 23.7 MB (23690146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1bc7c6cb691b4398568a3b72fd77c815d3b8bdbef595a06fd6bf5830771f7a`  
		Last Modified: Sat, 17 Aug 2024 08:12:54 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json
