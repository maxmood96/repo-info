## `ros:lunar-ros-core-zesty`

```console
$ docker pull ros@sha256:d2db241c4dc284adda5f3998247de92e3bccc6b0ef689956ca515866f5dd5c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:lunar-ros-core-zesty` - linux; amd64

```console
$ docker pull ros@sha256:0c6a19942aacac114d79c34f78d231d45364be50114d4e7e1fb68e4b5565d94c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (354968036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3eaba497107c57682fe5581486aef6286170c3b86ca4cac422eec5b24fbb38`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 Dec 2017 21:00:08 GMT
ADD file:796db5dd87a82ef3448e235015cbe46f6e917199753ab9fa0a7fc03d14da91b0 in / 
# Thu, 14 Dec 2017 21:00:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 14 Dec 2017 21:00:09 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 14 Dec 2017 21:00:10 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 14 Dec 2017 21:00:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 14 Dec 2017 21:00:11 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:45:44 GMT
RUN find /etc/apt/ -name *.list -exec sed -i -e 's/archive.ubuntu.com\|security.ubuntu.com/old-releases.ubuntu.com/g' {} \;
# Sat, 09 Dec 2023 02:45:55 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:45:56 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu zesty main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:45:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:46:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:46:54 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:46:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:47:23 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:47:23 GMT
ENV ROS_DISTRO=lunar
# Sat, 09 Dec 2023 02:49:41 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:49:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:49:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:49:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c2ca09a1934b951505ecc4d6b2e4ab7f9bf27bcdfb8999d0181deca74daf7683`  
		Last Modified: Thu, 14 Dec 2017 21:02:52 GMT  
		Size: 38.6 MB (38640200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c3619d2153ffdefa4a9c19f15c5d566ce271b397a84537baa9ee45b24178f2`  
		Last Modified: Thu, 14 Dec 2017 21:02:46 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efe07335a049e6afcd757db2d17ba37a12b717eb807acb03ddf3cd756b9fc2a`  
		Last Modified: Thu, 14 Dec 2017 21:02:46 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1bb01b3a3b72463ae8ac5666d57b28f1a21d5256271910ac8df841aa04ecd1`  
		Last Modified: Thu, 14 Dec 2017 21:02:46 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a98c1873995475a895f3d79f405232ef5230076b3f610c949c2e8341743af7`  
		Last Modified: Thu, 14 Dec 2017 21:02:46 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaa7efcea1ebaacadc918ee46d2be4c8dd7f9168ff4ec81f48099356b72f35c`  
		Last Modified: Sat, 09 Dec 2023 04:34:01 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3466ac680b3425e3778c7ef1a2cae696dd5c473755d0678d273c4da84d954e5`  
		Last Modified: Sat, 09 Dec 2023 04:34:02 GMT  
		Size: 5.0 MB (4979458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f98885729b4de3eb1dc872158d2fba501ab6dc2758b9493d7f9b9a67cf7b85`  
		Last Modified: Sat, 09 Dec 2023 04:34:00 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6dae4bb9df59219126cd33acb0d1fff869eb3f7db63e6b8102db3a8bbafef`  
		Last Modified: Sat, 09 Dec 2023 04:33:59 GMT  
		Size: 3.6 KB (3604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249f571155312897c3f3b98aefaafad38fbc25ba84244da487726b8fec98f5e5`  
		Last Modified: Sat, 09 Dec 2023 04:34:10 GMT  
		Size: 57.4 MB (57400596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1fe63f9eb4ad1998c517dea06034bf905f198978d7538418061edb2d36f35c`  
		Last Modified: Sat, 09 Dec 2023 04:33:59 GMT  
		Size: 1.6 MB (1611443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6f2f70e2e41b5b7f707fea113e5aaede9c85bc7a94ff8ab2a4e7e9a457b891`  
		Last Modified: Sat, 09 Dec 2023 04:34:41 GMT  
		Size: 252.3 MB (252329023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aee7e342c78bb814dd787acf203b5fb7284ab387dd6863dbb54899c4ddf84e`  
		Last Modified: Sat, 09 Dec 2023 04:33:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
