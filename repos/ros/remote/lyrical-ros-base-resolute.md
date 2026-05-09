## `ros:lyrical-ros-base-resolute`

```console
$ docker pull ros@sha256:2cdd3902d630fedfb33e7b2895034ce33d754f680f731df54e0009368a7a7db2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-base-resolute` - linux; amd64

```console
$ docker pull ros@sha256:ada79a1ecc3953db0685f65be8b3d1424ee4a54e36f38a63279745791461c580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339416490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b600ff5deebe2ec7fb32713eb68df3de542d12985c39b444d6388febd0582f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:19:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:19:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:19:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:20:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d78e0bbfc54960c1d9050e06e1fbb6b8e71dacf2cdb4d66cb6e015a8f7312`  
		Last Modified: Sat, 09 May 2026 00:21:04 GMT  
		Size: 124.7 MB (124737949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a44bf4030e5e86c84762608c8c70592d177e681192adfc99cbc6ee911d5546`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 372.9 KB (372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d20c0e84974b12eec6d14b04e2a6e9ad88f979d562e6fefa8af049ae36cfc5`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93e4853a5be4476dc8afdd04e48a0d4cf8913d7431b2850bb30bf7ac89ecbf`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 25.7 MB (25708500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:2e4f4a88aa22149b8f7902e32bcfc19b8ea3d8b3ead54c3a6054cb1a89281bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29031296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9d20c7af3df94a5babd40059a96bfe98295fabe87e3c4d432176d5e9ead06a`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ddced94e7b81222993cbf35ca699f7960ffd4373aa0c92dd78b4dda4e6baa`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 29.0 MB (29014138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8910a6bd8c9e6bbe5049c8ca9bd33484850a549cdfcbcdfe3da9a4c6f5f5ac32`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 17.2 KB (17158 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-base-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8548467e419ef69ecdf02a25c0f25d76173d9208e9597e98e6d43f57eb6a61a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324190553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2297e725c268af41131d851a5917cc5e187a2f99d46938128d4fc3a12c081d1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:17:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:17:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:17:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d616b9ddec74bbcb20aecbdb8529a143f8c7b16913e11f94e32199829327a93`  
		Last Modified: Sat, 09 May 2026 00:18:46 GMT  
		Size: 118.2 MB (118153470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c328c3b8daee7f1f707be08e1192ee6c9041f48302d1cd581895c3f543506`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 372.9 KB (372898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de351669d7d636b1fd95a81cd027b607bff48ac52729b84869644be0ee14ae`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 130.8 KB (130807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbf379aec8d97e3ab9091ff59091eb41363b0363c5bfec3929457e27e54b98`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 24.7 MB (24650366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:f3c9a13721bacb6b7d2236c2dd09ea5996f72f5ae9e50455ee034990d847a38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9030b2c11574415c78ab1905860db0c0796842c898ba7e09080735c4f739b12`

```dockerfile
```

-	Layers:
	-	`sha256:146db6f4e3ff1627ee09ede1d352f2fa38126c9d603435e2d45398e2fc7b36b4`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 29.1 MB (29077414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15c3d48e1916829dbecd4399e73a22884f3c1d69d4a19510db0d94495c1db47`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 17.3 KB (17295 bytes)  
		MIME: application/vnd.in-toto+json
