## `ros:kinetic-ros-core`

```console
$ docker pull ros@sha256:ea30c1f3f2864d2ae6c24e5108e7932b289ff2c0ef88e223469cb8ba5f690044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:aab52bbaeb4b9043eab8246e810bdbf34e5d2981a38873053c615cb37820bddc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299917212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4e8508393aa9c539787c9b28a2f544cafa62eb31e6383c4cc9d18243f0e4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 00:27:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:27:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 22 Feb 2020 00:27:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 22 Feb 2020 00:28:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:28:04 GMT
ENV LANG=C.UTF-8
# Sat, 22 Feb 2020 00:28:05 GMT
ENV LC_ALL=C.UTF-8
# Sat, 22 Feb 2020 00:28:05 GMT
ENV ROS_DISTRO=kinetic
# Sat, 22 Feb 2020 00:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 22 Feb 2020 00:29:21 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 00:29:22 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 22 Feb 2020 00:29:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 22 Feb 2020 00:29:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af5a2e269056c8d304ca70dbb3df8cb043049caa1593349c0567d2b1800926d`  
		Last Modified: Sat, 22 Feb 2020 00:48:46 GMT  
		Size: 6.9 MB (6936216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c8ea5750dd46479094654598598168f8632118dce36d0e00356d303689938e`  
		Last Modified: Sat, 22 Feb 2020 00:48:44 GMT  
		Size: 13.1 KB (13101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb110c86f88c42f992f9baba79944724cc65986e79d8626a415cb29b4421069`  
		Last Modified: Sat, 22 Feb 2020 00:48:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c8d1c05d52300d66a89da8dd24a045a5d0cbc2a44f695ecb7da34c5299e383`  
		Last Modified: Sat, 22 Feb 2020 00:48:58 GMT  
		Size: 54.8 MB (54776668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09500c9f9db2638ab3a5fd6b7d51a74befe9cafde1c5702f00c10a3ef7d83e4e`  
		Last Modified: Sat, 22 Feb 2020 00:48:43 GMT  
		Size: 425.0 KB (425030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbf4b9d57c61e0caef23140f26837706319c2b3370ebddc24a92b9434008fa5`  
		Last Modified: Sat, 22 Feb 2020 00:49:27 GMT  
		Size: 193.6 MB (193572507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e515d19e5c0b1ec72f4409b7a7c0ab7edaee124e3a6c39996a9d6d40897c2c6a`  
		Last Modified: Sat, 22 Feb 2020 00:48:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:57ccad6f8ce8efc61a0d234ec49967bcd361d4a0bb1c6641b8323436a20b2556
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260348784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c587ff89f3b2019e25b7d6cd5449acfb3e4b9f955bed6c5beeb48da3debdb3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Feb 2020 22:06:20 GMT
ADD file:7f245cd0bb5455d315f8d753720fab55e9ac41f68c7926b597663d3aeff3c8d4 in / 
# Fri, 21 Feb 2020 22:06:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:06:29 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:06:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:06:31 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:23:27 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:23:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 21 Feb 2020 22:23:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 21 Feb 2020 22:24:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:24:40 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2020 22:24:41 GMT
ENV LC_ALL=C.UTF-8
# Fri, 21 Feb 2020 22:24:42 GMT
ENV ROS_DISTRO=kinetic
# Fri, 21 Feb 2020 22:24:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 21 Feb 2020 22:27:21 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:27:29 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 21 Feb 2020 22:27:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 21 Feb 2020 22:27:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:957d6015142d0d6fe598b45df39c8f36d0b86fe61fdb145603423c7d216e5f09`  
		Last Modified: Mon, 17 Feb 2020 15:45:30 GMT  
		Size: 38.9 MB (38890364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a31e0e10e55fa8dad735b48b598b86efb29be81ae44906466ea04a2fd13c6c7`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c42599b1b7e867902cc3b4a6cd7cd76c9148ff337a0bc7861131b6176648b45`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33654ecb4a4aa4b3b5b7f650b7aab38e3fe0d8d48d88c666f052f819016c3d55`  
		Last Modified: Fri, 21 Feb 2020 22:07:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67149689ed2c2bdb9efa3be9211d193b8028cc4784db0d6619a9390627191a5`  
		Last Modified: Fri, 21 Feb 2020 22:54:51 GMT  
		Size: 5.7 MB (5700209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95330f9d14ca033d17600bc8d8b11608f55728260b78bb4fd27004e672c4678`  
		Last Modified: Fri, 21 Feb 2020 22:54:49 GMT  
		Size: 13.1 KB (13102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93b787c40ff4d82dfe37e2e0a7011c7931ed7cb0007f131e5d046c99a784b91`  
		Last Modified: Fri, 21 Feb 2020 22:54:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b3da0282c816c36e5a182050d37ab4ff20cdd608c07e25dc928ddd8ddf18bc`  
		Last Modified: Fri, 21 Feb 2020 22:55:06 GMT  
		Size: 50.3 MB (50348544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca1be963619c117704380dd2072975e251e911c6730b5b665535cdd33d12346`  
		Last Modified: Fri, 21 Feb 2020 22:54:47 GMT  
		Size: 423.3 KB (423280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafbfcd6ad198bc58083d92dde377c197dab923ea886b8d4ed0f04574e9262d2`  
		Last Modified: Fri, 21 Feb 2020 22:55:46 GMT  
		Size: 165.0 MB (164971335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c520232387742ece66353864fde9c0eec372ea161e352369fd19d93be7957`  
		Last Modified: Fri, 21 Feb 2020 22:54:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9f7c8e46026b0d00ddfe30cfca48d45a047312056c2856f1bfe233dfef5b9e03
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272670524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d7134f7a6893f5c73fb8df47838548a2b20923e018a595e9b7eb0878ef88a6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:07:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:07:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 21 Feb 2020 23:07:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 21 Feb 2020 23:08:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:08:34 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2020 23:08:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 21 Feb 2020 23:08:35 GMT
ENV ROS_DISTRO=kinetic
# Fri, 21 Feb 2020 23:08:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 21 Feb 2020 23:11:59 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:12:02 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 21 Feb 2020 23:12:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 21 Feb 2020 23:12:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de89c3a73198e1dda189ac912dee05355cade0a829922bd13857425957eda71`  
		Last Modified: Fri, 21 Feb 2020 23:40:57 GMT  
		Size: 6.0 MB (5958466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9106380c300220f4bd02ff0b4648f292c64d767c8207b4e0e71534d4dd38961`  
		Last Modified: Fri, 21 Feb 2020 23:40:54 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6208cdca92b9d0f49fd401ca56c0296caa856bf0b7b4f7d9af3ad99f4fa5ad32`  
		Last Modified: Fri, 21 Feb 2020 23:40:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b569144b519d956769fd4db1b95a39e8afc6a4ca3e4a238d203404f4d4ceac1`  
		Last Modified: Fri, 21 Feb 2020 23:41:12 GMT  
		Size: 52.1 MB (52072482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a928563a652cdfddfb1e6dfdd83e83025d93c4b82eddf246fbb8687af9ed7a1c`  
		Last Modified: Fri, 21 Feb 2020 23:40:53 GMT  
		Size: 423.6 KB (423576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ab00cc30c740bb1569b4705e648bc226ba65f277626e6aa9cd6a2d43557f3`  
		Last Modified: Fri, 21 Feb 2020 23:41:45 GMT  
		Size: 174.3 MB (174260615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f030f8f50f315846c4e32e83784be19ace559a52e3dd2cdf7926183de31bc00b`  
		Last Modified: Fri, 21 Feb 2020 23:40:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
