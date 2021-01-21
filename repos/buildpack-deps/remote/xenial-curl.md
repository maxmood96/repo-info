## `buildpack-deps:xenial-curl`

```console
$ docker pull buildpack-deps@sha256:38a2db9b2595d730f3f9ec7228859160df28205d9b37909365d7638b1596e2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:xenial-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:167c062ef0331e098640486f765bcffe4929cfb4b5b38c59e9fc744a03bf15b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53589395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25b9d68c10f7c66e19ab26d2d15b94fc24b6cc18e96b39783845c8f034aa84d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 17:19:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 17:19:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24d98811751655f4b386b1f42b38795c225d92edf069a4242ba4cde44129273`  
		Last Modified: Thu, 17 Dec 2020 17:33:57 GMT  
		Size: 7.7 MB (7749576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:47ccd6f44a57cbd6ff199c9fdebe5b59d815656c463fdf3210346db0adf0468e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46581446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d49769a1120788e5fbe08de456bae1ad01b765dff17df64db67c8238bcd92a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:17:15 GMT
ADD file:c77c1a2ea3c8b1d59252626e6c8be57cca539dfce0a16a0ed2ff0311c0f5a265 in / 
# Thu, 21 Jan 2021 03:17:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:17:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:17:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:17:26 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:08:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:08:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2af2a813aac2db23328a29ab84155e95fbb6681e872751a4f11f688c005e84c5`  
		Last Modified: Mon, 18 Jan 2021 19:38:27 GMT  
		Size: 40.0 MB (39972659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ef2a276bd8b4a122330892d4a9b9383249f945d22fc34e7b2b0688fbf6af8`  
		Last Modified: Thu, 21 Jan 2021 03:19:28 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01c8ce931ce58b3726d3fa387bcf38f02ca4a4d9fa6db2a764bb8aae4f69079`  
		Last Modified: Thu, 21 Jan 2021 03:19:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ba02aed017c06ce4541aa061d63a8068bd1651fc0f00b9c0995ec1b22bea3`  
		Last Modified: Thu, 21 Jan 2021 03:19:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfd57609ff2207dee9da91c92371b2df20fee94b6ad19388d93afa4c409ac0e`  
		Last Modified: Thu, 21 Jan 2021 04:18:58 GMT  
		Size: 6.6 MB (6607260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30883be1030cb8b713b953b858e1922120b9783510995b5abae3deba79e4c7b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47634967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543294295936d27f29b72bbae9c08ac1d0f95fa615113e9660bcd03c5451413d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:44:18 GMT
ADD file:a360b1e1db1ae9973dac11dfe4e549f6416e278f53c42eb5e98b3b3da8d2a5ae in / 
# Wed, 25 Nov 2020 22:44:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:44:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:44:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:44:26 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 10:31:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:31:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3e30c5e4609ac16f9e19faa3800699e28c77aadcfcbde2ddd5954606f80fa170`  
		Last Modified: Sat, 31 Oct 2020 00:25:13 GMT  
		Size: 40.8 MB (40826105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be82da0c7e998c509a8e86338f139501b62fde0df3908dd489a8249380ea3441`  
		Last Modified: Wed, 25 Nov 2020 22:45:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04dffef88e5257b2388d643e5fb03a812316de0737ce92e3888a6722cea5e`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624f7934929e6e67f81a9becb317179367648ec1236d644e9bf3a00d3fe3772`  
		Last Modified: Wed, 25 Nov 2020 22:45:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8a362be1f341ce825525591dd6d59ddf9c39c8e93fdb816fb504f50e20d277`  
		Last Modified: Thu, 17 Dec 2020 10:49:07 GMT  
		Size: 6.8 MB (6807373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2698011e7c8d30bdb337603ab93daea3b93263d8320ed5f315677dd873acbfaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53309117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d2ccbd7b7d7d2ce4ac8f8b377f32e39067806c06e3d338c7254fc255b14ca9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:44:39 GMT
ADD file:f0259b34ff9566a47759b946075a90b425b35071a6fcf4181253856267c482d1 in / 
# Thu, 21 Jan 2021 03:44:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:44:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:44:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:44:42 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:06:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c75068e8d6988b427382a590aa2d27221e0bd617b5c548855bc92a484a2ec6a4`  
		Last Modified: Mon, 18 Jan 2021 20:06:08 GMT  
		Size: 45.4 MB (45405564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43cb87a8c1bc5cbd0f326895a8822f29a84f8d2c44274f27f88103b5991a9f`  
		Last Modified: Thu, 21 Jan 2021 03:45:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055fac63ec310fd3d5f85f15fa5fd4d8cf42f416af240cfb7c915aad0b4cc12`  
		Last Modified: Thu, 21 Jan 2021 03:45:16 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cc5eaa9ba060369cb187a024e6a86791164acd2f430114d9282f03dd5edcc1`  
		Last Modified: Thu, 21 Jan 2021 03:45:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4222d5c1e96727a2a683004ba6948dd6907a69c59088abfb1f54a30c3488f642`  
		Last Modified: Thu, 21 Jan 2021 04:14:02 GMT  
		Size: 7.9 MB (7902013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e03e87151bb6d05ee78107946240184564d13f6847e8b45a60832d7c1dc48b2e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54671071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd40984ec6f6c3b9e32b9fa7fa3c8221d38acfe7d6e01deff7dd4ce7c6eb256`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:41 GMT
ADD file:77d4196b81aae0a74a7c06551cb151a1f9ce9c1f3c4cb68d72ecb7273dd0b401 in / 
# Wed, 25 Nov 2020 22:26:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:12 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 13:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 13:15:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:93c8cfbc1882e03d6a4c073c13b7cb3eff8981390da93bb1d41c058d8e8e9ec5`  
		Last Modified: Mon, 02 Nov 2020 23:21:43 GMT  
		Size: 47.0 MB (47012517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a39f498605e8790f2a442e0b5d71643611aa8812b32e47edc6e0fc1f3d322f`  
		Last Modified: Wed, 25 Nov 2020 22:28:46 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaa0c9b5e986ccc702029a50b231fe5441768e669984f5d2d72f24685295f4e`  
		Last Modified: Wed, 25 Nov 2020 22:28:46 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf553b562c201a12dd6f3fd40fb599513dd20f8bec6b48ad9745d70a95d014a8`  
		Last Modified: Wed, 25 Nov 2020 22:28:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f37defc53b3d6781139859a55fefcee7525c966f35d180e6bc069c9b820aa77`  
		Last Modified: Thu, 17 Dec 2020 14:05:04 GMT  
		Size: 7.7 MB (7657050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:xenial-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a4be8053a86133f10d1bb40c191f2bca74fd23c197e88d506d14bcbc38ce60c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51190224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961a6318a736319937521d9c7f9f8569d68332756c8a923f9eca00c34cefcf13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:46:32 GMT
ADD file:0abbb4e685f021a587e7647917ba1c9aa99b9c358596db8c0df3e300942fad02 in / 
# Wed, 25 Nov 2020 22:46:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:46:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:46:47 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:46:48 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 11:40:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:40:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1f02beb7696b5bef8510687ea530b1dbf3e5a28f378b27f55d35a262da449cc5`  
		Last Modified: Mon, 02 Nov 2020 23:24:00 GMT  
		Size: 43.7 MB (43697241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b7171e0d153041c02d0ef16df6b49317e4635caea3c959ae43ed366ec10b30`  
		Last Modified: Wed, 25 Nov 2020 22:47:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee86a115656e8574ffd79a10876cc26fb9ff7f104444d19b36034cf90d8a170`  
		Last Modified: Wed, 25 Nov 2020 22:47:59 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0969d0db5ddb84d5abc6aed3392ef2709c820548519455262102c0c20c82699d`  
		Last Modified: Wed, 25 Nov 2020 22:47:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e009e11608be75ce5ac0ec4a8d75ef35872b9d65d6b38551ea1776ffbbbcbc`  
		Last Modified: Thu, 17 Dec 2020 11:53:11 GMT  
		Size: 7.5 MB (7491496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
