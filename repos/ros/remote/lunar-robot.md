## `ros:lunar-robot`

```console
$ docker pull ros@sha256:ab0bf4049417d4a2dc626031952bccb919f5dc0ef396c2cce8c66029bfaa7250
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lunar-robot` - linux; amd64

```console
$ docker pull ros@sha256:be5eb026c00b7754193812da7ec1ae1101bb2974b1be3b2f4fcb8ab9952310cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.1 MB (492144942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69b3062ae4210b51554551f30ce0860bb82e09ac09f2591508f088f80882a3c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:57:44 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Thu, 26 Apr 2018 23:57:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 26 Apr 2018 23:57:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV ROS_DISTRO=lunar
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Fri, 13 Dec 2024 13:12:07 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Fri, 13 Dec 2024 13:09:14 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Fri, 13 Dec 2024 13:10:06 GMT  
		Size: 528.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Fri, 13 Dec 2024 13:08:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ab159a07291d742304920b79c14160def8f59b0960a09de2153cbf3a713fd`  
		Last Modified: Fri, 06 Jun 2025 22:49:42 GMT  
		Size: 6.9 MB (6939367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666f4344c057c7c79a8c767c35606fe7237d0cd03cd578070204607a24e0e571`  
		Last Modified: Fri, 06 Jun 2025 22:49:42 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadeec5d2aa49358a0c95bd28186e5e1870a47b03258f31b31473b785d42b9de`  
		Last Modified: Fri, 06 Jun 2025 22:49:42 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fec28c4ac90e93fc866c6a9b249cb5f4010680060934e03a1aff4f744c9a9e`  
		Last Modified: Fri, 06 Jun 2025 22:49:45 GMT  
		Size: 54.3 MB (54251263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab75082b9a09a85d411d21349d8ff5f1dddcca35b0c3839e40debbd3dd3f5f8`  
		Last Modified: Fri, 06 Jun 2025 22:49:43 GMT  
		Size: 1.9 MB (1907618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f6e124e3717740ec2bf06672e9200ec6bfe1fcc81a965c1df1b909a4f48b4`  
		Last Modified: Fri, 06 Jun 2025 23:07:36 GMT  
		Size: 193.4 MB (193351670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5957640ad151f4165dfcde4c0b4fb8e9b288ea790956b366caae5e98cfd354`  
		Last Modified: Fri, 06 Jun 2025 22:49:43 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e953e55cf55f11499636b0be8fdb31b2d51399d7215f3a67ef02a7375f7d3e`  
		Last Modified: Fri, 06 Jun 2025 23:09:41 GMT  
		Size: 85.5 MB (85456298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f95607fa4e488f943210a4f9fd0c974cb80d3dd9c2ba872414b6a74602fcf0`  
		Last Modified: Sat, 07 Jun 2025 00:09:58 GMT  
		Size: 103.7 MB (103721861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-robot` - unknown; unknown

```console
$ docker pull ros@sha256:790f2a62927dcf228a24e5e97a964ed2d7313941eac0f451ea6dc140bf6319a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45973313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e8056d91fb9b80f22538f678e66e8dc6d5f932f2be429e176b905b42f746cf`

```dockerfile
```

-	Layers:
	-	`sha256:d13a779e998c5ad68113e9d08582cd5259296a402fd00901c05c0e7c9662c471`  
		Last Modified: Sat, 07 Jun 2025 01:23:14 GMT  
		Size: 46.0 MB (45963430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4370b38119029de5c38189cfe7681268325048490b463eb4b58a83d10de7eb8d`  
		Last Modified: Sat, 07 Jun 2025 01:23:15 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lunar-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:2d48119bfc8d263bc0bc05b3fc201ad36ebdbf83df4d121d81cddb94dba1fc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.8 MB (428801550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bfd129edde30d0e6d1dad3664cb41f8acc3a518323b32577079abdc2001384`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:57:44 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Thu, 26 Apr 2018 23:57:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 26 Apr 2018 23:57:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV ROS_DISTRO=lunar
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Tue, 17 Dec 2024 15:12:14 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67de3a011d085fbb829ef04d78536904c6ead23dbc82dd5facff2488d6398672`  
		Last Modified: Sat, 14 Dec 2024 10:56:05 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1202719f1ed95c66ca12784e9dd1983de008b6871eb2cb324c3a3f1a98836af`  
		Last Modified: Sat, 14 Dec 2024 08:45:37 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1764d93e99e79b6b91814768fa379cc5ce0dce26c71ecfe2f5fc6b3f38212b`  
		Last Modified: Sat, 14 Dec 2024 13:56:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a9efacdb733c2fb39076b37dded86a88cd62fb1c74b5515c47335180243e4`  
		Last Modified: Fri, 06 Jun 2025 23:03:39 GMT  
		Size: 5.7 MB (5701655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03abd5568e0f21ac1a88810d2f1a7440e11e213f902e4c43890cbedfb489fdfd`  
		Last Modified: Fri, 06 Jun 2025 23:03:38 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9306ee55967f6fad73271d8e982eca09e95cb37c8eea8b50f0f6c54add2989a1`  
		Last Modified: Fri, 06 Jun 2025 23:03:39 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c057727f274d15046b615f58bb89163e07f83ea6fd3943da66919914bd1513bf`  
		Last Modified: Fri, 06 Jun 2025 23:03:43 GMT  
		Size: 49.8 MB (49808908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc840338cf675e9a2e2c82f4582a509063786f887976fea9b34241b922ada4`  
		Last Modified: Fri, 06 Jun 2025 23:03:41 GMT  
		Size: 1.9 MB (1907403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251c334d8191461a21685b6aa412beb8445bba6aca0e123bcb18395b350b72a6`  
		Last Modified: Sat, 07 Jun 2025 11:56:38 GMT  
		Size: 164.7 MB (164735620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038d0131f890f5cd0d702c5171fef1b8c3599a0a363c4d8cc840646cedae7a0`  
		Last Modified: Fri, 06 Jun 2025 23:03:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5ca64cbbcd8d0a7a1aabee0d47ef2c86d1e78456a0039fbe20d076370bb96`  
		Last Modified: Fri, 06 Jun 2025 23:20:38 GMT  
		Size: 76.2 MB (76230375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fc7f4fd276ec7f3e082d7276640368af2f1d8878f0ef10589749fe4829447f`  
		Last Modified: Sat, 07 Jun 2025 11:58:02 GMT  
		Size: 90.1 MB (90086032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-robot` - unknown; unknown

```console
$ docker pull ros@sha256:ef191dd27bd2156416f2824661a56696e81edf1ebd30dc10bfe717bf4129c49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45532427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c50d06afe7160983f75a6e4a8c2c00b1831315798e3e8a6852a89552fefa130`

```dockerfile
```

-	Layers:
	-	`sha256:3d4adf040932106ee480a104d4b60b14dc58abaf180c6a790bd0fcb9a1e9ca72`  
		Last Modified: Sat, 07 Jun 2025 01:24:00 GMT  
		Size: 45.5 MB (45522438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b181a4ade86cb1d84be0da3433b32354247f983ef0c6424ca953f490874ddc`  
		Last Modified: Sat, 07 Jun 2025 01:24:01 GMT  
		Size: 10.0 KB (9989 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lunar-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55d9081ee95433271b2dcad91db8059b7fc4ee7c71768f8962f991ce33956520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.4 MB (446374013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3a150df9724a8f9b00e98bf7037decefb8b1579de28b855a489f371d4a642`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Apr 2018 23:57:44 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Thu, 26 Apr 2018 23:57:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 26 Apr 2018 23:57:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["/bin/bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LANG=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Apr 2018 23:57:44 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENV ROS_DISTRO=lunar
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Apr 2018 23:57:44 GMT
CMD ["bash"]
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Apr 2018 23:57:44 GMT
RUN apt-get update && apt-get install -y     ros-lunar-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Fri, 13 Dec 2024 17:43:40 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66927c6d1d3d2e9321c4893f7f2105b7cd23dfb082853d97ec08f188e271e612`  
		Last Modified: Fri, 13 Dec 2024 20:27:34 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000560be91651dcbf476ebacb8bf1f1339694a3327f8e6da2519e0b29b33eb5d`  
		Last Modified: Fri, 13 Dec 2024 18:38:28 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6225a0253717abdc2ee23ea211c1c439c93b84231ec0a4f1c74762a205ba7234`  
		Last Modified: Fri, 13 Dec 2024 13:19:32 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c3c7fa1dbf39c02c8e143a34d21d21ae8a213708dfa93636973101fbe6dfb4`  
		Last Modified: Fri, 06 Jun 2025 22:54:04 GMT  
		Size: 6.0 MB (5958484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9af9636c74800d8fb80c3b306c34b804106f114cf8e2a716011bb8f623d680`  
		Last Modified: Fri, 06 Jun 2025 22:54:03 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823d15c61da62ded6603fed3d8bd7c3ee85b7d90d7ab2c255a2623657a583a39`  
		Last Modified: Fri, 06 Jun 2025 22:54:03 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62e0a751f3a49a05f6cdbfe23f772012565e57c354bf85df6155cfc3337bd87`  
		Last Modified: Fri, 06 Jun 2025 22:54:06 GMT  
		Size: 51.6 MB (51559430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf119c02c68eda54d4cf53ec3a4606e3ae7771e1b917dcd7cb8788b81f6c9859`  
		Last Modified: Fri, 06 Jun 2025 22:54:05 GMT  
		Size: 1.9 MB (1907544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0456cf71714a073a4eb9bbc79b5b3f3d4b08efc0069182646fcbd0d31547d7a4`  
		Last Modified: Sat, 07 Jun 2025 11:56:22 GMT  
		Size: 174.0 MB (173995768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de28b75411d2e198fcf0f41d3b67eeb48b62ece3bcdb053a8239534cc6a91b`  
		Last Modified: Fri, 06 Jun 2025 22:54:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29828e69108e5f7e56f0bae6be5e4b62fd37bbe48356fe19ebba33d7e56f3f6`  
		Last Modified: Sat, 07 Jun 2025 11:56:40 GMT  
		Size: 77.7 MB (77711863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79adfe71266ddd200269de7c2ae8dfafc4485a11328b26a8c7b2f481eaea76e6`  
		Last Modified: Sat, 07 Jun 2025 11:57:36 GMT  
		Size: 94.0 MB (93982403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lunar-robot` - unknown; unknown

```console
$ docker pull ros@sha256:24fa2ced09db30e70466ac844a10396524a8dbf96c6da96c80d4dfab252830d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45662733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73529c878486b2b60ffaae68cc42e8d3dbdee21f1ab6cdd02a4c505c6d7ab84a`

```dockerfile
```

-	Layers:
	-	`sha256:7b96871ec6fcbd09df4dfea1071a12ebe38ff7406ec54df3d43e167c857e4538`  
		Last Modified: Sat, 07 Jun 2025 01:24:51 GMT  
		Size: 45.7 MB (45652723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3dbb729c21789ef35332be6788188b014e8f3f7cf7b76efde934d30f564cce`  
		Last Modified: Sat, 07 Jun 2025 01:24:52 GMT  
		Size: 10.0 KB (10010 bytes)  
		MIME: application/vnd.in-toto+json
