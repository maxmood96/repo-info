## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:cc89c6ba2e1f5da876052102bd88329336dfd405c2076611eebb449203ce5cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:d16d411c2de4bdb9dbd792e146be49cbc6801321829ea16a825215df35eb5be8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322059503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3816f11bdde39731fba61a16ee620c21d47f9d0e706a50275d2e8c2d2283753`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:20 GMT
ADD file:6e16bc9cf28c19a1fb1fb516411643e33cbd2bdb7b6c2ce2468c6583c89871a2 in / 
# Tue, 09 Jun 2020 01:23:21 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 20:24:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 20:24:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 09 Jun 2020 20:24:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 09 Jun 2020 20:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 20:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Jun 2020 20:24:26 GMT
ENV ROS_DISTRO=melodic
# Tue, 09 Jun 2020 20:26:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 20:26:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 09 Jun 2020 20:26:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Jun 2020 20:26:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:81fc1918191541a2ffb6ed1cd8386ef8302aea1b0613ebc768a00e76c1f34bb9`  
		Last Modified: Tue, 09 Jun 2020 01:27:59 GMT  
		Size: 45.4 MB (45375796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e53c331f2ecda6ec4f9119258b0b88f1dc218bc1e67ba82cb01a51942b25544`  
		Last Modified: Tue, 09 Jun 2020 20:37:22 GMT  
		Size: 6.9 MB (6865099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f44dc7569baa1eebbc5e1f5560794048d8ba35421873de7531310f8082c0c7`  
		Last Modified: Tue, 09 Jun 2020 20:37:20 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948152c2814e825ed688e3a3048f639f0fb3eccef07021e0a0d6e15f3be182ea`  
		Last Modified: Tue, 09 Jun 2020 20:37:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4136b73b353797b6cf84a63c456c39bb9485b7b1447f2c6616474dd330da2`  
		Last Modified: Tue, 09 Jun 2020 20:39:21 GMT  
		Size: 269.8 MB (269816794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651404712d7315cbd7e8cebf1f5c9b0d54a0c8b3d60974a39b80501691b64794`  
		Last Modified: Tue, 09 Jun 2020 20:37:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6ba7a8b8eae966d9127a05d888a4a2e8716345ed4a13ae0bafb2f4d90120b306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274557102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564cf86c9eeac8ce9680956f3e596d98af1c2cc32fb6171d918fa5534b9e1014`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 12:53:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 12:53:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 09 Jun 2020 12:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 09 Jun 2020 12:53:46 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 12:53:47 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Jun 2020 12:53:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 09 Jun 2020 12:56:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 12:56:58 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 09 Jun 2020 12:56:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Jun 2020 12:57:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37f88e51d5d4beec1083e08e9be466763532cf657032a2c3c98008435fef6bc`  
		Last Modified: Tue, 09 Jun 2020 13:19:38 GMT  
		Size: 6.4 MB (6437966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe875459741248032e30abc4885c469fed8a4ebc05c8631c30f33195652c661`  
		Last Modified: Tue, 09 Jun 2020 13:19:37 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c097c91b719aef58bd93f194a36cc365038154109f7f7511d360e3d53f89c9`  
		Last Modified: Tue, 09 Jun 2020 13:19:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052064a7c891cb66765fc80001209186d5d9afb261c8827deee3450f5b19602a`  
		Last Modified: Tue, 09 Jun 2020 13:20:42 GMT  
		Size: 225.0 MB (224956393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9498708f5b05239cb64faf42e52aecdcb33660842377e40ff0c61c1c363c996`  
		Last Modified: Tue, 09 Jun 2020 13:19:37 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
