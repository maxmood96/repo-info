## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:e72c0539c7edcdb779223a29ada0c0e57bd26825bd0005b787cf9d418c687209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:0bba4f36ac9f9e797aee9a420c10a111397f5f4d05b19429b0c3e6c578f6ba9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463363754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f05059606cd7f18f9bae4a272bf4a607309d6c3a28241b4f76ddd4ee93c78d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 12:48:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 12:48:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Jun 2022 12:48:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Jun 2022 12:48:09 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 12:48:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Jun 2022 12:48:09 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Jun 2022 12:49:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 12:49:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 23 Jun 2022 12:49:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Jun 2022 12:49:11 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 12:49:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 12:49:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 23 Jun 2022 12:50:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d614310471c61e4200046b8f7adea9e8513871ad4fde9b669e49cafd656bde2`  
		Last Modified: Thu, 23 Jun 2022 12:53:58 GMT  
		Size: 10.9 MB (10892280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c90706f4c8a053c5c76e44d43756ced985189146b36ac63497e25ceceefc5c5`  
		Last Modified: Thu, 23 Jun 2022 12:53:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832307bf10c44d39b4524638f32d96d980cbea1925cc229df4ca7c97c3d08e81`  
		Last Modified: Thu, 23 Jun 2022 12:53:57 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09580d323567b8cc4622a787e2540c618939571a6ba340dd72e42597029cbba5`  
		Last Modified: Thu, 23 Jun 2022 12:54:29 GMT  
		Size: 239.2 MB (239166199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dee1b44de370322d2b90ea5963fab4508b3ab8cb639137e6550b9b3b4e1067`  
		Last Modified: Thu, 23 Jun 2022 12:53:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532db9983a02cf12facfbc9d855d8b0d8017f91070219df3a2b34b2e47e1af91`  
		Last Modified: Thu, 23 Jun 2022 12:54:49 GMT  
		Size: 86.6 MB (86570833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3c90a928c35eea266dcd4b163632518a2ba34fec87e85be9da72c8e28fd4ac`  
		Last Modified: Thu, 23 Jun 2022 12:54:36 GMT  
		Size: 314.9 KB (314932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408082b6be6f30efe6639d4c71c063e39a4d63d9421fa7934cce66402953ff82`  
		Last Modified: Thu, 23 Jun 2022 12:54:46 GMT  
		Size: 76.0 MB (75976290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:01f74d9b338be7c30df3edd29edd868f3d18e37b96b1b68866846bf1d742f673
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402832375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d432918317d5267e0a9c4bece83cd67ca946c4bf56fca69ffd142c2dd91555c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:54 GMT
ADD file:a5e3c0ffa9f9754a6d77fafd8288e699a70f7f6ff7c5912a065f1c69f1393e99 in / 
# Thu, 23 Jun 2022 00:40:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 13:15:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:15:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Jun 2022 13:15:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Jun 2022 13:15:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 13:15:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Jun 2022 13:15:43 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Jun 2022 13:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:17:01 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 23 Jun 2022 13:17:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Jun 2022 13:17:04 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 13:17:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:17:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 23 Jun 2022 13:18:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d6f1451981514e25c21542f5c7ee9bb90052b8856b484ce47294cbf1fd5a234`  
		Last Modified: Thu, 23 Jun 2022 00:47:46 GMT  
		Size: 49.2 MB (49229092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcd1485b8f3c07588c4ea63df43ce191dc4bd704f4db66afbba5befa84a13c3`  
		Last Modified: Thu, 23 Jun 2022 13:24:26 GMT  
		Size: 10.7 MB (10688303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a806e582281d47bb169333c62fc3d5d3d9478b1b26ec2c797fde052f7e0e3d2c`  
		Last Modified: Thu, 23 Jun 2022 13:24:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be161c8e6aa95e3bf58f9376749c867ab58036e812be1274d6a856816a5f07e5`  
		Last Modified: Thu, 23 Jun 2022 13:24:25 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba910dea9270aeab8bd65e0a16c91c62e0b2be0bae0732297f397d380a67c9a9`  
		Last Modified: Thu, 23 Jun 2022 13:24:55 GMT  
		Size: 184.4 MB (184373444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1a9512c8212e5a0c18aa9cd30761ed21b47f629705aa14f6d2ecbb65c5b129`  
		Last Modified: Thu, 23 Jun 2022 13:24:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bce340567d35b4721c009c051ef26145127e7720e3e18709788b179372804ae`  
		Last Modified: Thu, 23 Jun 2022 13:25:19 GMT  
		Size: 84.4 MB (84359150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bea8aaf3bd8c5a8e329e1d5e484cb74d7da63aa6ea2cb85d7e1a4c80c5b51b`  
		Last Modified: Thu, 23 Jun 2022 13:25:08 GMT  
		Size: 314.9 KB (314884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b642d19a1b3158f3f5972ee91bc146fad2f8df02d4dbb3a715bffbdb7c1273`  
		Last Modified: Thu, 23 Jun 2022 13:25:18 GMT  
		Size: 73.9 MB (73865133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
