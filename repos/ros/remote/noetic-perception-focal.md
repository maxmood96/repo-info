## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:bd87a0440d97e738f8166fbfaf6b42ba7e06a44cc6d8ccc897c3b66288726924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:282dd9085542968f2236e813cfdd39c0289a250805b71295c916b568e1aac04e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **831.3 MB (831289980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9983b8470d111e88fe2adb5a30eabf79803355b685be14648190ee8c0ca0e2b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d20b699901600cccce48488414a9dd0422d2895492730687aa8adef23a7b687`  
		Last Modified: Thu, 03 Mar 2022 23:25:24 GMT  
		Size: 491.9 MB (491948492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:4523fda981e7422844b7f1e51b0ee3fc802299b1362c0be612c583337b98544e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.1 MB (721114502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7e660599567d0d130ff0f3b07814a32df28654472fe0974aa59d64a3159cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b4c7a328f0c55d991752acd1e86f087cee7829349dc21b75beb8b1ee74989f`  
		Last Modified: Wed, 02 Feb 2022 03:46:12 GMT  
		Size: 436.3 MB (436281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f91e6d5ad30903ca659a9e6465dadff5a434900146a4b17c8fdb7613f1457f2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.8 MB (780835119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4ba87571080cec8f30b7a3856f03b4a37cefcb6266c40c2f9d25ba80fab48d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df905bd7e0288b9a41622859f12eee9a1eac351afa894a89a9c8037e37854c5b`  
		Last Modified: Thu, 03 Mar 2022 21:43:45 GMT  
		Size: 462.5 MB (462476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
