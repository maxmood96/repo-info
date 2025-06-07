## `ros:jade-perception-trusty`

```console
$ docker pull ros@sha256:ef0cb9f8ac054c7101659290be8ddc0a22005c0bbddd24be1cee1c3f3e3b9559
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `ros:jade-perception-trusty` - linux; amd64

```console
$ docker pull ros@sha256:9f8f54395c09a07ea893ea1de56791f7e2ae4b0b102eb73b3fca508ce6c38d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.3 MB (534283821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0772fa35153bb94356672ed83575c565ec00940215756cd08ef572c4a50f2ac8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Sep 2017 19:26:55 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Mon, 11 Sep 2017 19:26:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 11 Sep 2017 19:26:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["/bin/bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LANG=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV ROS_DISTRO=jade
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-base=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-perception=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Fri, 13 Dec 2024 13:52:03 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Fri, 13 Dec 2024 14:33:56 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Fri, 13 Dec 2024 13:28:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7947e2e80596bd2dd6aa721c50543b02d859c18c479e6fee7974186341fbf`  
		Last Modified: Fri, 06 Jun 2025 22:50:20 GMT  
		Size: 14.0 MB (13999678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53493d080ac5b1dcf02f0544ab568f501bbd0cd25d5a3d4c090f79cfade15863`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b7382600e2675b92184b3c9e606962fb3a31d0fcc797c9718d86c5aeb77e1`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0540af077fd693d6d887b2c1377227d8aca763ac4abce016145113d53735c2`  
		Last Modified: Fri, 06 Jun 2025 22:50:21 GMT  
		Size: 30.9 MB (30903820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a90e857d50dc2639933dc58909049bb48dc5e49480f0b333cf30fd28555667d`  
		Last Modified: Fri, 06 Jun 2025 22:50:37 GMT  
		Size: 1.9 MB (1907624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d6930123b937d48d4d52a308e963df7fcdc06810cc42be7feaafbc10e10241`  
		Last Modified: Fri, 06 Jun 2025 23:07:49 GMT  
		Size: 149.7 MB (149666410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a118e840e02939fac45745192b1b0256e7a176b68dd4d15b726e57f220d86`  
		Last Modified: Fri, 06 Jun 2025 22:50:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b08e9e2a9e663ee9d05790e491d44762dc6ef429870e731c93a8d91ad0ff0d`  
		Last Modified: Sat, 07 Jun 2025 00:07:53 GMT  
		Size: 3.6 MB (3588314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2adf87410b14d7c7791392c33acdbbc41334482656ccb823e8d5515299dc881`  
		Last Modified: Sat, 07 Jun 2025 00:11:00 GMT  
		Size: 263.4 MB (263437423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jade-perception-trusty` - unknown; unknown

```console
$ docker pull ros@sha256:b157de88d57575274212d0124a1cc8cfcfec343d20fb8d54d5bf447a444f40dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46373540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f0a3eed2f34930319e3aee67c6be458048bf220fb0bbbfa7b789c7778eb5c`

```dockerfile
```

-	Layers:
	-	`sha256:73926cf0909c038bc3983147c2d0eeddbac02c45d62ace2166c8a30563cde817`  
		Last Modified: Sat, 07 Jun 2025 01:21:14 GMT  
		Size: 46.4 MB (46363927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d6360b775d4d5c16158e331b48b37748929466a00016a42d1ff8693415e786`  
		Last Modified: Sat, 07 Jun 2025 01:21:15 GMT  
		Size: 9.6 KB (9613 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jade-perception-trusty` - linux; arm variant v7

```console
$ docker pull ros@sha256:8a3700e8223addbe734114f19356b08041adb70d21808e47cd5c14037bfa36b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.0 MB (482040322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5993a2dd91ba780131db62d446d884b3f3d0ca306f8a5bb21aed97eda2d90d81`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Sep 2017 19:26:55 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Mon, 11 Sep 2017 19:26:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 11 Sep 2017 19:26:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["/bin/bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LANG=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 Sep 2017 19:26:55 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENV ROS_DISTRO=jade
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Sep 2017 19:26:55 GMT
CMD ["bash"]
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-base=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Sep 2017 19:26:55 GMT
RUN apt-get update && apt-get install -y     ros-jade-perception=1.2.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Tue, 14 Jan 2025 21:10:21 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31831ce9fd9e38ad9d926286efdb85e400dc823da723d72cc676869c295fb0`  
		Last Modified: Sat, 14 Dec 2024 10:55:47 GMT  
		Size: 76.8 KB (76775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66373b79ee1bedb2a2bf237fb2a717660559ee8e3fec0aae52d9797c2b32b27c`  
		Last Modified: Tue, 14 Jan 2025 21:05:11 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca3ba35474a2e7add4548570538f01ba4e19ba476ef013e6894b61ee78fc57f`  
		Last Modified: Fri, 06 Jun 2025 22:52:08 GMT  
		Size: 12.4 MB (12355346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3a1499d5668b6eeb89a9466248af62e9ca582a05b6194ab6e3d02eee5dc26e`  
		Last Modified: Fri, 06 Jun 2025 22:55:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8938a18f64a189658ee8f48b5e9f7a626ff41fcf30c5f874cb2abb63d68ef65f`  
		Last Modified: Fri, 06 Jun 2025 22:55:37 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263cbdaf4bc7d3a241568d22257a71f9904927c34f31958e9158bce6ef124d42`  
		Last Modified: Fri, 06 Jun 2025 22:55:39 GMT  
		Size: 28.4 MB (28374521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a92fe5263a2bc487b090e21e20f621403dbf2bbe128fd8708aba520322cceda`  
		Last Modified: Fri, 06 Jun 2025 22:55:39 GMT  
		Size: 1.9 MB (1907400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e4d6c3244eb00fe78adf5d790629099bc764bb9edc1c0c19c2e6e30a138bfe`  
		Last Modified: Fri, 06 Jun 2025 22:55:14 GMT  
		Size: 137.3 MB (137281787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f438e1a65e86df020def93be8ab1a263a07888112d72daaf1891da6b229ace`  
		Last Modified: Fri, 06 Jun 2025 22:55:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a3b5e16317ffd998270388053df05039b291855511acb39b0134904a2a00ae`  
		Last Modified: Fri, 06 Jun 2025 23:15:34 GMT  
		Size: 3.2 MB (3239276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ba6057d586a193b1b913e615f036912e80a189369f14808fb933bd40b4f88`  
		Last Modified: Sat, 07 Jun 2025 00:20:35 GMT  
		Size: 234.2 MB (234164917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jade-perception-trusty` - unknown; unknown

```console
$ docker pull ros@sha256:c986bb08d22efbe203f57b28764441712e5d63e5e1b19732d1fe241d84fe80ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46501893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031ed3287a28b2f46eba7b8fae99995816be7cf081a37e342258b37056ff5ae5`

```dockerfile
```

-	Layers:
	-	`sha256:59f93ef1fd9cb8884932f51c35a9859f0ddf05ec369986f1e806f4fec123d864`  
		Last Modified: Sat, 07 Jun 2025 01:22:15 GMT  
		Size: 46.5 MB (46492184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a3e2e04aace724a1c4769144d3c0efa90d5ee1351f97e133122141ab22717c0`  
		Last Modified: Sat, 07 Jun 2025 01:22:16 GMT  
		Size: 9.7 KB (9709 bytes)  
		MIME: application/vnd.in-toto+json
