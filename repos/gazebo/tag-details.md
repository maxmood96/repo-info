<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gazebo`

-	[`gazebo:gzserver10`](#gazebogzserver10)
-	[`gazebo:gzserver10-bionic`](#gazebogzserver10-bionic)
-	[`gazebo:gzserver11`](#gazebogzserver11)
-	[`gazebo:gzserver11-bionic`](#gazebogzserver11-bionic)
-	[`gazebo:gzserver11-focal`](#gazebogzserver11-focal)
-	[`gazebo:gzserver7`](#gazebogzserver7)
-	[`gazebo:gzserver7-xenial`](#gazebogzserver7-xenial)
-	[`gazebo:gzserver9`](#gazebogzserver9)
-	[`gazebo:gzserver9-bionic`](#gazebogzserver9-bionic)
-	[`gazebo:gzserver9-stretch`](#gazebogzserver9-stretch)
-	[`gazebo:gzserver9-xenial`](#gazebogzserver9-xenial)
-	[`gazebo:latest`](#gazebolatest)
-	[`gazebo:libgazebo10`](#gazebolibgazebo10)
-	[`gazebo:libgazebo10-bionic`](#gazebolibgazebo10-bionic)
-	[`gazebo:libgazebo11`](#gazebolibgazebo11)
-	[`gazebo:libgazebo11-bionic`](#gazebolibgazebo11-bionic)
-	[`gazebo:libgazebo11-focal`](#gazebolibgazebo11-focal)
-	[`gazebo:libgazebo7`](#gazebolibgazebo7)
-	[`gazebo:libgazebo7-xenial`](#gazebolibgazebo7-xenial)
-	[`gazebo:libgazebo9`](#gazebolibgazebo9)
-	[`gazebo:libgazebo9-bionic`](#gazebolibgazebo9-bionic)
-	[`gazebo:libgazebo9-stretch`](#gazebolibgazebo9-stretch)
-	[`gazebo:libgazebo9-xenial`](#gazebolibgazebo9-xenial)

## `gazebo:gzserver10`

```console
$ docker pull gazebo@sha256:1113f905a739556e2484690fcd86765fa21a8550dbece831346c07423aef0cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver10` - linux; amd64

```console
$ docker pull gazebo@sha256:5dec980563d40333514ed322a0b8bdeb029d42148702fc191b5b0a64d5778c1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268487279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2bd08bd1a7ccdba23e99b16361f28b0bef9600133609b9599b49205c7f6a3b`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:06:48 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:06:48 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:06:48 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:06:48 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6a32c4f72367f5709d855a46f4a5ee39df84e1e4267a9a5c7ced3e793ac23`  
		Last Modified: Thu, 04 Mar 2021 04:20:18 GMT  
		Size: 226.2 MB (226227727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91743264d4edbe70a25141d36e0449fe212318c7bed42bd54b3a48822f15b9f`  
		Last Modified: Thu, 04 Mar 2021 04:19:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver10-bionic`

```console
$ docker pull gazebo@sha256:1113f905a739556e2484690fcd86765fa21a8550dbece831346c07423aef0cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver10-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:5dec980563d40333514ed322a0b8bdeb029d42148702fc191b5b0a64d5778c1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268487279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2bd08bd1a7ccdba23e99b16361f28b0bef9600133609b9599b49205c7f6a3b`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:06:48 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:06:48 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:06:48 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:06:48 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6a32c4f72367f5709d855a46f4a5ee39df84e1e4267a9a5c7ced3e793ac23`  
		Last Modified: Thu, 04 Mar 2021 04:20:18 GMT  
		Size: 226.2 MB (226227727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91743264d4edbe70a25141d36e0449fe212318c7bed42bd54b3a48822f15b9f`  
		Last Modified: Thu, 04 Mar 2021 04:19:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:446082d5fc8a1db994499884a49c8448e02f3406d29216ad1286ada441af1195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:b14dcfd42081207dd3d37b3903da74a69134c603200d1413ae69b65815d1c09e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318606681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9db29628c66c5aadd66a400faad75332fe9160f6b851892c4d3a170a4505289`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:11:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:12:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:12:02 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:14:14 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:14:15 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6feb7b35b48a6d7b9001d90f52185993d6984828fb9c5eb938874fe345fab7d`  
		Last Modified: Thu, 04 Mar 2021 04:22:47 GMT  
		Size: 1.2 MB (1182675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c853d2c4ffee69978054a176e77e8291024992e917d83428d5a5edb1b89ba43a`  
		Last Modified: Thu, 04 Mar 2021 04:22:49 GMT  
		Size: 16.1 MB (16147927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5984595a6c793e11621cfb81d492c34889df12e312e22f65f434e627ac62c1a`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498dca1a259e8ce35a3e98981a85038e8c7b651b1b646209014cb6b41fe456`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4bd9ce9f5d6bf9474f5ff72468be5a9e1462094bc6d5f6454f5e3c89311de`  
		Last Modified: Thu, 04 Mar 2021 04:23:24 GMT  
		Size: 272.7 MB (272700186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acd4e790058155c9721c0b77b961fc5d4989c9c948ae1be62e2a602a609e6f`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:a3adaef365bd8a21ccecdd481f442c91b2322eba1daf0b4193dbfc26c0a39814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:2f975ac15042c1f377fc361a2ae07acb658755e738687bef3bc9ce00da2b8cd9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277703870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f714782dcf8c51b394c006e44b8a877acc731d46f6c8819064bf8cff54f31158`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:09:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:09:47 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:09:47 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:09:47 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:09:48 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95064ebc38c682903e3822849e9730a14fb2839ab9a9eaba3fec6bdae7254a3`  
		Last Modified: Thu, 04 Mar 2021 04:21:53 GMT  
		Size: 235.4 MB (235444318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8abb2ffebf81aba6fcaf408dd9cf21a42e153efe446f66159e3646037c6b52`  
		Last Modified: Thu, 04 Mar 2021 04:21:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:446082d5fc8a1db994499884a49c8448e02f3406d29216ad1286ada441af1195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:b14dcfd42081207dd3d37b3903da74a69134c603200d1413ae69b65815d1c09e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318606681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9db29628c66c5aadd66a400faad75332fe9160f6b851892c4d3a170a4505289`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:11:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:12:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:12:02 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:14:14 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:14:15 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6feb7b35b48a6d7b9001d90f52185993d6984828fb9c5eb938874fe345fab7d`  
		Last Modified: Thu, 04 Mar 2021 04:22:47 GMT  
		Size: 1.2 MB (1182675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c853d2c4ffee69978054a176e77e8291024992e917d83428d5a5edb1b89ba43a`  
		Last Modified: Thu, 04 Mar 2021 04:22:49 GMT  
		Size: 16.1 MB (16147927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5984595a6c793e11621cfb81d492c34889df12e312e22f65f434e627ac62c1a`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498dca1a259e8ce35a3e98981a85038e8c7b651b1b646209014cb6b41fe456`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4bd9ce9f5d6bf9474f5ff72468be5a9e1462094bc6d5f6454f5e3c89311de`  
		Last Modified: Thu, 04 Mar 2021 04:23:24 GMT  
		Size: 272.7 MB (272700186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acd4e790058155c9721c0b77b961fc5d4989c9c948ae1be62e2a602a609e6f`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver7`

```console
$ docker pull gazebo@sha256:0e1cdd68ce453cd9e0caea9ce89d798b67db99544db67987bb90db838ba53d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver7` - linux; amd64

```console
$ docker pull gazebo@sha256:ded3727474304ba062ccfdfa9261928d13744077d2a04b177ec59ccb8fde1d45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243910208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad815b2ec4129e47e114f361444cd4f0f292810613573b1c862968250dbcc8eb`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:20:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 21 Jan 2021 08:20:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 21 Jan 2021 08:21:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:21:50 GMT
EXPOSE 11345
# Thu, 21 Jan 2021 08:21:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 21 Jan 2021 08:21:50 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 21 Jan 2021 08:21:51 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bfc4631203bea4266dcc3b7096abf253420b839ea92d6269b460d7d48b4c4f`  
		Last Modified: Thu, 21 Jan 2021 08:46:24 GMT  
		Size: 16.3 MB (16281985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4580897c4cd70506d0594700a9cd00f64793818db0b29fe2dc737381fba91`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38dcf8a227a6d57e11c3b7726be2c8d8a5dcdc96c5be0dc30f40404e2fa8ea`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6610063116e71214a9a5c0d903f620d3842d1e4eeef2d63945aaa20e62e6fa`  
		Last Modified: Thu, 21 Jan 2021 08:46:49 GMT  
		Size: 181.6 MB (181643856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6338dba92c9ea9e70ac08548ebb2b69465fcc2f46eb17d6974077707566a5a1`  
		Last Modified: Thu, 21 Jan 2021 08:46:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver7-xenial`

```console
$ docker pull gazebo@sha256:0e1cdd68ce453cd9e0caea9ce89d798b67db99544db67987bb90db838ba53d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver7-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:ded3727474304ba062ccfdfa9261928d13744077d2a04b177ec59ccb8fde1d45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243910208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad815b2ec4129e47e114f361444cd4f0f292810613573b1c862968250dbcc8eb`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:20:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 21 Jan 2021 08:20:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 21 Jan 2021 08:21:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:21:50 GMT
EXPOSE 11345
# Thu, 21 Jan 2021 08:21:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 21 Jan 2021 08:21:50 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 21 Jan 2021 08:21:51 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bfc4631203bea4266dcc3b7096abf253420b839ea92d6269b460d7d48b4c4f`  
		Last Modified: Thu, 21 Jan 2021 08:46:24 GMT  
		Size: 16.3 MB (16281985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4580897c4cd70506d0594700a9cd00f64793818db0b29fe2dc737381fba91`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38dcf8a227a6d57e11c3b7726be2c8d8a5dcdc96c5be0dc30f40404e2fa8ea`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6610063116e71214a9a5c0d903f620d3842d1e4eeef2d63945aaa20e62e6fa`  
		Last Modified: Thu, 21 Jan 2021 08:46:49 GMT  
		Size: 181.6 MB (181643856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6338dba92c9ea9e70ac08548ebb2b69465fcc2f46eb17d6974077707566a5a1`  
		Last Modified: Thu, 21 Jan 2021 08:46:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:51b8b0d854a3d315d43dd9f6338d269dc3ba732ac573f2cd7f7c825841281fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:33ba4ecfe3ba0f5f97c1ebec23154d0bbfc94f7917768784fad6bbe6361087bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268600655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a84113a0fd46f10e4e3c1309f58d5d910aa510eaae527a33cb52f7c841d675`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:52 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:03:52 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:03:52 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:03:53 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2c851523c97e4363b92141c4aa336d7b84ebf59db5d10d5cdf44c10660e64b`  
		Last Modified: Thu, 04 Mar 2021 04:18:52 GMT  
		Size: 226.3 MB (226341103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38115e1f11af59104be8cea9e0b86f261892fc3f3213eea3ee0828c0d2ac9b0`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-bionic`

```console
$ docker pull gazebo@sha256:51b8b0d854a3d315d43dd9f6338d269dc3ba732ac573f2cd7f7c825841281fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:33ba4ecfe3ba0f5f97c1ebec23154d0bbfc94f7917768784fad6bbe6361087bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268600655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a84113a0fd46f10e4e3c1309f58d5d910aa510eaae527a33cb52f7c841d675`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:52 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:03:52 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:03:52 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:03:53 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2c851523c97e4363b92141c4aa336d7b84ebf59db5d10d5cdf44c10660e64b`  
		Last Modified: Thu, 04 Mar 2021 04:18:52 GMT  
		Size: 226.3 MB (226341103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38115e1f11af59104be8cea9e0b86f261892fc3f3213eea3ee0828c0d2ac9b0`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:d1b5f1f17e6fc7bbeec18006a2a422a29328b7514cb693d23acebbb67c416e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:ff1eb621c4c1d1678e69b479e2697d7d09c99e1a95ea14ab33539549720d12ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266174829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b76fff5b37194e38c6630ac3d9c98217997803b0d7a1f683158b85f7715450`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:50:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:51:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 09 Feb 2021 05:51:04 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 09 Feb 2021 05:51:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:51:56 GMT
EXPOSE 11345
# Tue, 09 Feb 2021 05:51:56 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 09 Feb 2021 05:51:57 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 09 Feb 2021 05:51:57 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d04da106e9d8decd06fcae16919ea213b53cb7d5cb11b8ae89ba23f8de520f`  
		Last Modified: Tue, 09 Feb 2021 05:55:01 GMT  
		Size: 18.5 MB (18510153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a07071cedc4afa32c43e5d8b2f88c01823bbaac433a582c14f7653d07070`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a63a19aca85323515410a8b69b99d8755c6fcf2ab40928b157064bbed8b6df1`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 5.0 KB (4983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340534c7d3270cf1864dbe33bd8d3c5366247424abf6fd9a18ecf86f067708c9`  
		Last Modified: Tue, 09 Feb 2021 05:55:35 GMT  
		Size: 202.3 MB (202278200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d1a164683b13cace62a43ac21634c54ed3b6dd3b8b63a22afa21bfb2bc318`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-xenial`

```console
$ docker pull gazebo@sha256:14eaf492480fb0d2eaa7dacb288d6914e2f7c5089f4bbf9df686b2f90e5d2918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:071f21f35878ba4451d5e6c549f3355b448aa49fa3cb9c237c8d037e3f5747c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270603681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610dd125ad83cae249f5291664ff33a51baff509a43df45d326211cbfa103684`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:20:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 21 Jan 2021 08:20:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 21 Jan 2021 08:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:25:09 GMT
EXPOSE 11345
# Thu, 21 Jan 2021 08:25:09 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 21 Jan 2021 08:25:09 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 21 Jan 2021 08:25:10 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bfc4631203bea4266dcc3b7096abf253420b839ea92d6269b460d7d48b4c4f`  
		Last Modified: Thu, 21 Jan 2021 08:46:24 GMT  
		Size: 16.3 MB (16281985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4580897c4cd70506d0594700a9cd00f64793818db0b29fe2dc737381fba91`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38dcf8a227a6d57e11c3b7726be2c8d8a5dcdc96c5be0dc30f40404e2fa8ea`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960a27279f1cb88dc7661fc108f0ac994b0d65f72c5144839c6fa8d5ff307cf0`  
		Last Modified: Thu, 21 Jan 2021 08:48:38 GMT  
		Size: 208.3 MB (208337330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc3b12772417e22924dd172b6979965b13208e4edf1335c2986e8c0aadb570f`  
		Last Modified: Thu, 21 Jan 2021 08:47:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:latest`

```console
$ docker pull gazebo@sha256:3d0b9a0201a4f6f75085a1b74c37c1b5bfb3aa188506c48c1f82380d447e6ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:544fca97b5b405c4e40592d06186bd70688e6d513c080aab6e445b7d9150ace3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 MB (599058555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893946cb1618012e1a18dd46e9bf99d3ca09806df68e9792282050a3e8e00d4`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:11:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:12:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:12:02 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:14:14 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:14:15 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:17:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6feb7b35b48a6d7b9001d90f52185993d6984828fb9c5eb938874fe345fab7d`  
		Last Modified: Thu, 04 Mar 2021 04:22:47 GMT  
		Size: 1.2 MB (1182675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c853d2c4ffee69978054a176e77e8291024992e917d83428d5a5edb1b89ba43a`  
		Last Modified: Thu, 04 Mar 2021 04:22:49 GMT  
		Size: 16.1 MB (16147927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5984595a6c793e11621cfb81d492c34889df12e312e22f65f434e627ac62c1a`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498dca1a259e8ce35a3e98981a85038e8c7b651b1b646209014cb6b41fe456`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4bd9ce9f5d6bf9474f5ff72468be5a9e1462094bc6d5f6454f5e3c89311de`  
		Last Modified: Thu, 04 Mar 2021 04:23:24 GMT  
		Size: 272.7 MB (272700186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acd4e790058155c9721c0b77b961fc5d4989c9c948ae1be62e2a602a609e6f`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d017f41d33a93d8be291a8d53fccc0318959949d6b8823df8262980e1891da1`  
		Last Modified: Thu, 04 Mar 2021 04:24:24 GMT  
		Size: 280.5 MB (280451874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo10`

```console
$ docker pull gazebo@sha256:8751c4b27b8dcac3e527bd9bbf310b2eba2c7ebf99f34131dcf47d6ead1271ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo10` - linux; amd64

```console
$ docker pull gazebo@sha256:69f1c245ba9b246a3ff9aa0eea3612fbb62b3247531fcaaec347813fb02f2e70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 MB (522102075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4b85f43f36f96233f3df9fe3cc2cd617d1718fa3c7fdfc4e3b469898dec410`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:06:48 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:06:48 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:06:48 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:06:48 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:08:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo10-dev=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6a32c4f72367f5709d855a46f4a5ee39df84e1e4267a9a5c7ced3e793ac23`  
		Last Modified: Thu, 04 Mar 2021 04:20:18 GMT  
		Size: 226.2 MB (226227727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91743264d4edbe70a25141d36e0449fe212318c7bed42bd54b3a48822f15b9f`  
		Last Modified: Thu, 04 Mar 2021 04:19:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c315bde239facfcacabbf6edb55f2b4b1ea994cf83d72aeb4e2d6c42a9cf00`  
		Last Modified: Thu, 04 Mar 2021 04:21:10 GMT  
		Size: 253.6 MB (253614796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo10-bionic`

```console
$ docker pull gazebo@sha256:8751c4b27b8dcac3e527bd9bbf310b2eba2c7ebf99f34131dcf47d6ead1271ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo10-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:69f1c245ba9b246a3ff9aa0eea3612fbb62b3247531fcaaec347813fb02f2e70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 MB (522102075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4b85f43f36f96233f3df9fe3cc2cd617d1718fa3c7fdfc4e3b469898dec410`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:06:48 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:06:48 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:06:48 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:06:48 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:08:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo10-dev=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6a32c4f72367f5709d855a46f4a5ee39df84e1e4267a9a5c7ced3e793ac23`  
		Last Modified: Thu, 04 Mar 2021 04:20:18 GMT  
		Size: 226.2 MB (226227727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91743264d4edbe70a25141d36e0449fe212318c7bed42bd54b3a48822f15b9f`  
		Last Modified: Thu, 04 Mar 2021 04:19:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c315bde239facfcacabbf6edb55f2b4b1ea994cf83d72aeb4e2d6c42a9cf00`  
		Last Modified: Thu, 04 Mar 2021 04:21:10 GMT  
		Size: 253.6 MB (253614796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:3d0b9a0201a4f6f75085a1b74c37c1b5bfb3aa188506c48c1f82380d447e6ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:544fca97b5b405c4e40592d06186bd70688e6d513c080aab6e445b7d9150ace3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 MB (599058555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893946cb1618012e1a18dd46e9bf99d3ca09806df68e9792282050a3e8e00d4`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:11:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:12:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:12:02 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:14:14 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:14:15 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:17:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6feb7b35b48a6d7b9001d90f52185993d6984828fb9c5eb938874fe345fab7d`  
		Last Modified: Thu, 04 Mar 2021 04:22:47 GMT  
		Size: 1.2 MB (1182675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c853d2c4ffee69978054a176e77e8291024992e917d83428d5a5edb1b89ba43a`  
		Last Modified: Thu, 04 Mar 2021 04:22:49 GMT  
		Size: 16.1 MB (16147927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5984595a6c793e11621cfb81d492c34889df12e312e22f65f434e627ac62c1a`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498dca1a259e8ce35a3e98981a85038e8c7b651b1b646209014cb6b41fe456`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4bd9ce9f5d6bf9474f5ff72468be5a9e1462094bc6d5f6454f5e3c89311de`  
		Last Modified: Thu, 04 Mar 2021 04:23:24 GMT  
		Size: 272.7 MB (272700186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acd4e790058155c9721c0b77b961fc5d4989c9c948ae1be62e2a602a609e6f`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d017f41d33a93d8be291a8d53fccc0318959949d6b8823df8262980e1891da1`  
		Last Modified: Thu, 04 Mar 2021 04:24:24 GMT  
		Size: 280.5 MB (280451874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:d9f04f5d01bf8f4799fe2fd35b8723e5d2c6dd48adb60a398661cc345f3c2398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:d6470802e3ce5998290907884cf9d88e426959153b7a8f2328a4447479254d6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.0 MB (547041512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6542b2c04ac4dd6813ae82dd1b022cd31a246a4c38ab7440195ec36b9e0de6d`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:09:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:09:47 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:09:47 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:09:47 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:09:48 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95064ebc38c682903e3822849e9730a14fb2839ab9a9eaba3fec6bdae7254a3`  
		Last Modified: Thu, 04 Mar 2021 04:21:53 GMT  
		Size: 235.4 MB (235444318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8abb2ffebf81aba6fcaf408dd9cf21a42e153efe446f66159e3646037c6b52`  
		Last Modified: Thu, 04 Mar 2021 04:21:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49b2fb1abfd8fd9ebbe76b78d76415f59cddeba968646c0b0dfc8369c05cd04`  
		Last Modified: Thu, 04 Mar 2021 04:22:42 GMT  
		Size: 269.3 MB (269337642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:3d0b9a0201a4f6f75085a1b74c37c1b5bfb3aa188506c48c1f82380d447e6ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:544fca97b5b405c4e40592d06186bd70688e6d513c080aab6e445b7d9150ace3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 MB (599058555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7893946cb1618012e1a18dd46e9bf99d3ca09806df68e9792282050a3e8e00d4`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:11:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:12:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:12:02 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:14:14 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:14:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:14:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:14:15 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:17:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.3.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6feb7b35b48a6d7b9001d90f52185993d6984828fb9c5eb938874fe345fab7d`  
		Last Modified: Thu, 04 Mar 2021 04:22:47 GMT  
		Size: 1.2 MB (1182675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c853d2c4ffee69978054a176e77e8291024992e917d83428d5a5edb1b89ba43a`  
		Last Modified: Thu, 04 Mar 2021 04:22:49 GMT  
		Size: 16.1 MB (16147927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5984595a6c793e11621cfb81d492c34889df12e312e22f65f434e627ac62c1a`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f498dca1a259e8ce35a3e98981a85038e8c7b651b1b646209014cb6b41fe456`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c4bd9ce9f5d6bf9474f5ff72468be5a9e1462094bc6d5f6454f5e3c89311de`  
		Last Modified: Thu, 04 Mar 2021 04:23:24 GMT  
		Size: 272.7 MB (272700186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acd4e790058155c9721c0b77b961fc5d4989c9c948ae1be62e2a602a609e6f`  
		Last Modified: Thu, 04 Mar 2021 04:22:46 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d017f41d33a93d8be291a8d53fccc0318959949d6b8823df8262980e1891da1`  
		Last Modified: Thu, 04 Mar 2021 04:24:24 GMT  
		Size: 280.5 MB (280451874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo7`

```console
$ docker pull gazebo@sha256:7e961bbb2072b528a10052aba642c5825c749c5f964141f1f354c221b14d17ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo7` - linux; amd64

```console
$ docker pull gazebo@sha256:61cd7ee037f8834b2ba567c4c6af494a979cddd83625aa902a37abbc361a907d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.3 MB (484319519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f179c765a39881d87be3e8bd27f48f0fc91f4778bf3c0126edd189fefd30f8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:20:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 21 Jan 2021 08:20:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 21 Jan 2021 08:21:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:21:50 GMT
EXPOSE 11345
# Thu, 21 Jan 2021 08:21:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 21 Jan 2021 08:21:50 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 21 Jan 2021 08:21:51 GMT
CMD ["gzserver"]
# Thu, 21 Jan 2021 08:24:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo7-dev=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bfc4631203bea4266dcc3b7096abf253420b839ea92d6269b460d7d48b4c4f`  
		Last Modified: Thu, 21 Jan 2021 08:46:24 GMT  
		Size: 16.3 MB (16281985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4580897c4cd70506d0594700a9cd00f64793818db0b29fe2dc737381fba91`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38dcf8a227a6d57e11c3b7726be2c8d8a5dcdc96c5be0dc30f40404e2fa8ea`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6610063116e71214a9a5c0d903f620d3842d1e4eeef2d63945aaa20e62e6fa`  
		Last Modified: Thu, 21 Jan 2021 08:46:49 GMT  
		Size: 181.6 MB (181643856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6338dba92c9ea9e70ac08548ebb2b69465fcc2f46eb17d6974077707566a5a1`  
		Last Modified: Thu, 21 Jan 2021 08:46:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21c657ca3a128ce8d8736afe3f3ef9b4b237d63aac71b1eb0e3c3dce829b93c`  
		Last Modified: Thu, 21 Jan 2021 08:47:48 GMT  
		Size: 240.4 MB (240409311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo7-xenial`

```console
$ docker pull gazebo@sha256:7e961bbb2072b528a10052aba642c5825c749c5f964141f1f354c221b14d17ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo7-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:61cd7ee037f8834b2ba567c4c6af494a979cddd83625aa902a37abbc361a907d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.3 MB (484319519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f179c765a39881d87be3e8bd27f48f0fc91f4778bf3c0126edd189fefd30f8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:20:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 21 Jan 2021 08:20:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 21 Jan 2021 08:21:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:21:50 GMT
EXPOSE 11345
# Thu, 21 Jan 2021 08:21:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 21 Jan 2021 08:21:50 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 21 Jan 2021 08:21:51 GMT
CMD ["gzserver"]
# Thu, 21 Jan 2021 08:24:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo7-dev=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bfc4631203bea4266dcc3b7096abf253420b839ea92d6269b460d7d48b4c4f`  
		Last Modified: Thu, 21 Jan 2021 08:46:24 GMT  
		Size: 16.3 MB (16281985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4580897c4cd70506d0594700a9cd00f64793818db0b29fe2dc737381fba91`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38dcf8a227a6d57e11c3b7726be2c8d8a5dcdc96c5be0dc30f40404e2fa8ea`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6610063116e71214a9a5c0d903f620d3842d1e4eeef2d63945aaa20e62e6fa`  
		Last Modified: Thu, 21 Jan 2021 08:46:49 GMT  
		Size: 181.6 MB (181643856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6338dba92c9ea9e70ac08548ebb2b69465fcc2f46eb17d6974077707566a5a1`  
		Last Modified: Thu, 21 Jan 2021 08:46:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21c657ca3a128ce8d8736afe3f3ef9b4b237d63aac71b1eb0e3c3dce829b93c`  
		Last Modified: Thu, 21 Jan 2021 08:47:48 GMT  
		Size: 240.4 MB (240409311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9`

```console
$ docker pull gazebo@sha256:dafb7ca592502af281b79ccce279ab087f019970b8c333dc729b9b2c1a5bcbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9` - linux; amd64

```console
$ docker pull gazebo@sha256:12311b0bcea6ed5b204c940421527653b4a1a0d0dfa6b6f4aad585637c99ae32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413800086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338aa1c8898fd9de2cfcb2146d82f8aa96c8afadaa800b2f2c86a0c80ffe8a11`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:52 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:03:52 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:03:52 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:03:53 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2c851523c97e4363b92141c4aa336d7b84ebf59db5d10d5cdf44c10660e64b`  
		Last Modified: Thu, 04 Mar 2021 04:18:52 GMT  
		Size: 226.3 MB (226341103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38115e1f11af59104be8cea9e0b86f261892fc3f3213eea3ee0828c0d2ac9b0`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94064730068f263fa2c869a8b75607e2296958f0fd8af7f8bd1601f81460839`  
		Last Modified: Thu, 04 Mar 2021 04:19:35 GMT  
		Size: 145.2 MB (145199431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:dafb7ca592502af281b79ccce279ab087f019970b8c333dc729b9b2c1a5bcbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:12311b0bcea6ed5b204c940421527653b4a1a0d0dfa6b6f4aad585637c99ae32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413800086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338aa1c8898fd9de2cfcb2146d82f8aa96c8afadaa800b2f2c86a0c80ffe8a11`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:52 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:03:52 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:03:52 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:03:53 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2c851523c97e4363b92141c4aa336d7b84ebf59db5d10d5cdf44c10660e64b`  
		Last Modified: Thu, 04 Mar 2021 04:18:52 GMT  
		Size: 226.3 MB (226341103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38115e1f11af59104be8cea9e0b86f261892fc3f3213eea3ee0828c0d2ac9b0`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94064730068f263fa2c869a8b75607e2296958f0fd8af7f8bd1601f81460839`  
		Last Modified: Thu, 04 Mar 2021 04:19:35 GMT  
		Size: 145.2 MB (145199431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:20a2cfd8188bdd63f924fe38d5980b201605fdf9ef3af54582e74cdc0dafdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:df3d52b9d2979760c41e9dad31bbdab765c319c2500aedae1cd6a2568b8ec72b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570181339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74df9839b29da66d1b1c27692e4bce45219dc62456fa368d049f2dd8e56cd147`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:50:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:51:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 09 Feb 2021 05:51:04 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 09 Feb 2021 05:51:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 05:51:56 GMT
EXPOSE 11345
# Tue, 09 Feb 2021 05:51:56 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 09 Feb 2021 05:51:57 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 09 Feb 2021 05:51:57 GMT
CMD ["gzserver"]
# Tue, 09 Feb 2021 05:53:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d04da106e9d8decd06fcae16919ea213b53cb7d5cb11b8ae89ba23f8de520f`  
		Last Modified: Tue, 09 Feb 2021 05:55:01 GMT  
		Size: 18.5 MB (18510153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a07071cedc4afa32c43e5d8b2f88c01823bbaac433a582c14f7653d07070`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a63a19aca85323515410a8b69b99d8755c6fcf2ab40928b157064bbed8b6df1`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 5.0 KB (4983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340534c7d3270cf1864dbe33bd8d3c5366247424abf6fd9a18ecf86f067708c9`  
		Last Modified: Tue, 09 Feb 2021 05:55:35 GMT  
		Size: 202.3 MB (202278200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5d1a164683b13cace62a43ac21634c54ed3b6dd3b8b63a22afa21bfb2bc318`  
		Last Modified: Tue, 09 Feb 2021 05:54:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3affd38e09b9da42cc8adc6cca2f1fcd2a475e97bb864f7edaf707bdb78df95b`  
		Last Modified: Tue, 09 Feb 2021 05:56:55 GMT  
		Size: 304.0 MB (304006510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:e7b42957c735136edd005ca46c6c14ba5685b3fb9557d0c89a7635c2ef11b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:b92d9d10ae2c204964152e7848dfd4eb99000eefd1225d55a345c0330c3947bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495311753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f06747a5c90fd5b0921fb10bb8eb9f8522bdf2aa95d843a6532fd59dc8e506`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:20:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 21 Jan 2021 08:20:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 21 Jan 2021 08:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 08:25:09 GMT
EXPOSE 11345
# Thu, 21 Jan 2021 08:25:09 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 21 Jan 2021 08:25:09 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 21 Jan 2021 08:25:10 GMT
CMD ["gzserver"]
# Thu, 21 Jan 2021 08:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bfc4631203bea4266dcc3b7096abf253420b839ea92d6269b460d7d48b4c4f`  
		Last Modified: Thu, 21 Jan 2021 08:46:24 GMT  
		Size: 16.3 MB (16281985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4580897c4cd70506d0594700a9cd00f64793818db0b29fe2dc737381fba91`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38dcf8a227a6d57e11c3b7726be2c8d8a5dcdc96c5be0dc30f40404e2fa8ea`  
		Last Modified: Thu, 21 Jan 2021 08:46:20 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960a27279f1cb88dc7661fc108f0ac994b0d65f72c5144839c6fa8d5ff307cf0`  
		Last Modified: Thu, 21 Jan 2021 08:48:38 GMT  
		Size: 208.3 MB (208337330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc3b12772417e22924dd172b6979965b13208e4edf1335c2986e8c0aadb570f`  
		Last Modified: Thu, 21 Jan 2021 08:47:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f444bdfa48e322c7f7d90e52dc31fdd22dce2a5237d0d9f4a9a5eca1b56a0c`  
		Last Modified: Thu, 21 Jan 2021 08:49:33 GMT  
		Size: 224.7 MB (224708072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
