## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:7b1853b398e14d491b62c92166bb1c2956e0b42d9cff6e0d9732e784c6584b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4091985e8ab9d2a5ec548e56a8074969e69edc59d78b82b3782f0513ce5331ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38836085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32756943e91e5ac2e3aa393697f6a4b08e8c7250af587581b61ed0290e33dbf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:45 GMT
ADD file:8cda7bfcf6c3010f9498acf5db465d8affd86bacb786338974486e23ea62b05d in / 
# Fri, 24 Jul 2020 14:38:46 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:46 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:47 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:47 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:02:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5f55bfaf77a136f7c6b5063e591480c2e7690ed1c29b0ee354caf8f6c62741e0`  
		Last Modified: Fri, 24 Jul 2020 14:39:44 GMT  
		Size: 28.4 MB (28357957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef373180da2631c7a56d9629e37de8010fe57414453617dde3a2c1e9861f1eb`  
		Last Modified: Fri, 24 Jul 2020 14:39:39 GMT  
		Size: 31.8 KB (31838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675d10b513df5337d26a6e2ccaf4875267999084d7f0d2f3102c54d7430cfa35`  
		Last Modified: Fri, 24 Jul 2020 14:39:39 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552f92805e8c6585c466083ac60f40092ae127e794d498c599a31bd67df21c09`  
		Last Modified: Fri, 24 Jul 2020 14:39:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c003fe1ffd7eb86efa0bcd0d127f5dca3b2f9dcaa3ad54bdeaaf16602fff1a`  
		Last Modified: Fri, 24 Jul 2020 15:10:39 GMT  
		Size: 6.9 MB (6859149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935824be9d9e08e1fe2b607c81e88e8128e36b84b36bdb20dfbc6a90fd43d96`  
		Last Modified: Fri, 24 Jul 2020 15:10:38 GMT  
		Size: 3.6 MB (3586137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9549c1bbb08c4128e0ee4f64d9e3e79caf06683ab394d45901428c122ce663df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32793204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ddad8b08d1fb3cf28da7e730fb92c8484cc1a889ef8b852c55187630d52e03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:07:21 GMT
ADD file:52d86d22ed47d0da1087414482ade7e5bded2a6a8d539e7214a7f6433820de24 in / 
# Fri, 24 Jul 2020 16:07:34 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:08:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:08:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:08:41 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:04:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:04:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:abee97477daae5ba1c098c334fa7126af27e46cb55f92383c47ee4752cca6b34`  
		Last Modified: Fri, 24 Jul 2020 16:17:36 GMT  
		Size: 23.8 MB (23847354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6932344878e72d9fc106f6b10714cc0590c46ab1bed3d33b7f005de5e8f44dad`  
		Last Modified: Fri, 24 Jul 2020 16:17:30 GMT  
		Size: 31.9 KB (31864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73c3d9eb80a07ca3c2917ec92d98f1dc20cce68119a1400b6dd5598ed03e90e`  
		Last Modified: Fri, 24 Jul 2020 16:17:29 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642ef31c2598b6d4f19ef5a77988b491517e1fd8fe77d266651b8bf97f76fa25`  
		Last Modified: Fri, 24 Jul 2020 16:17:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008346aa10ac7df0c83143808a07b8375543583d95413a44e8e1bab5b6251e1d`  
		Last Modified: Fri, 24 Jul 2020 18:16:31 GMT  
		Size: 5.9 MB (5853924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dea61df2b5ee1ad726d6997941e7635f818dc693712deaa4f8f12e426042aa`  
		Last Modified: Fri, 24 Jul 2020 18:16:30 GMT  
		Size: 3.1 MB (3059025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b31b2765046c3b083e1136b6fea9dd135cabe64bff1634f16d66adefeed544ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37285639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04afda55b58f7df6eaba6ba10940020863a97b03f471ea219e3a90c827664ad0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:25:04 GMT
ADD file:d70c9745470cda91695a18f189dd80bae5a680e704e1763095d25b73d54b3a74 in / 
# Fri, 24 Jul 2020 16:25:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:25:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:25:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:25:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:47:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:48:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ba5c49f251d9cd367877b4bb56a54c6c2cd649877fc1f3866a8c116211dcb43`  
		Last Modified: Fri, 24 Jul 2020 16:27:37 GMT  
		Size: 27.0 MB (26957842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869d6f4731727c8eee5a616ee243640c38bfd44a35c601ca60f3f8976637c7c8`  
		Last Modified: Fri, 24 Jul 2020 16:27:30 GMT  
		Size: 31.8 KB (31835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e46e1d5ec59f731bb7c1ef190b7269114c504db02a71b24bf310a987fb74a0`  
		Last Modified: Fri, 24 Jul 2020 16:27:29 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7393ecc5b169f761ed9ca88de6fc2aed57f05f141499a65a0f1bbeb2244b9b04`  
		Last Modified: Fri, 24 Jul 2020 16:27:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c679ba0ef5981a1712dde80261c3396ec19af33b91955f35f8045fea2fbaadc0`  
		Last Modified: Fri, 24 Jul 2020 18:56:57 GMT  
		Size: 6.7 MB (6724582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c54579b8207a09cbec12808075f84c215cd402182b4397a09750b63c52f85c0`  
		Last Modified: Fri, 24 Jul 2020 18:56:54 GMT  
		Size: 3.6 MB (3570345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3f03f0e1c43b8d0bcacad1076dfac435f16b82b4d2df77b551d7f36d15e5c95a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45247850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52b302f9dbe0ddc8f4552cabf964492309d21139cf82595ddca4c24ed9be115`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:37:12 GMT
ADD file:c00451f5cfe44d733a24fd1ed2ffcd58dd03d160b3be1f23a23c6988bfdde5f9 in / 
# Fri, 24 Jul 2020 14:37:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:37:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:12 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:29:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:30:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3ef413e40463b2cc51faddfd43a7ccebc442b8f3e610f2099c9b9f43ab4c794c`  
		Last Modified: Fri, 24 Jul 2020 14:43:13 GMT  
		Size: 33.0 MB (32952629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4a2aa97dce56eeeb38597752e261e49aa1782887302c44ab406af8642599fc`  
		Last Modified: Fri, 24 Jul 2020 14:43:07 GMT  
		Size: 31.7 KB (31677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0098b0f09cf883a00d68448733220790bdd0cf13bdbf30b747c84687fa0ca2`  
		Last Modified: Fri, 24 Jul 2020 14:43:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f899dca8f8bc39cfcda10bb89d224e2d1b4dbcb2a0c7d0b2bfd4e11bd11f0f61`  
		Last Modified: Fri, 24 Jul 2020 14:43:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f316702b922618a7a9bbe6a4ba46d737e166db8c781e15bc3e62b7895e72a4aa`  
		Last Modified: Fri, 24 Jul 2020 19:20:00 GMT  
		Size: 7.8 MB (7815065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62398f1446e8445ee9f855bf3fd20e927777bc1267fea9901b7204bd161a0f5`  
		Last Modified: Fri, 24 Jul 2020 19:19:59 GMT  
		Size: 4.4 MB (4447440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bee82c38d4cf8bb663c545e980228079457f3a94528b364a85e00fb37cbd9374
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37391608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774c96419e684afabfaff13dbdb51e1f8e6a15b138e28862597754cc8605586a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:44:39 GMT
ADD file:c2305b9c6b3d1f88851d28a75f00aefa09cd090dceed56cea0be0ef7848de90d in / 
# Fri, 24 Jul 2020 14:44:46 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:50:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:50:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:96ee9d07fad79c13f98051a8b3a80c5aa966b8b8e5c86f129811fc3e03c6a937`  
		Last Modified: Fri, 24 Jul 2020 14:46:02 GMT  
		Size: 27.2 MB (27230132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e509548444259d3ffae6be4cff91bdbd942e76236063786c133bd7a9916cb74`  
		Last Modified: Fri, 24 Jul 2020 14:45:58 GMT  
		Size: 32.5 KB (32481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af8f70e0f28da9bf410c9369c787d38fdd7d9bf805098562a6a4aefe14c3a`  
		Last Modified: Fri, 24 Jul 2020 14:45:58 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13885bcf94b5ef67414fbe9d1bc297ddc27a295f43fef37c3e0b67cb4449003e`  
		Last Modified: Fri, 24 Jul 2020 14:45:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26680f14729a94627c13dc3cd3045f620296504b41dcdcfaf2743d8d425014f0`  
		Last Modified: Fri, 24 Jul 2020 16:49:11 GMT  
		Size: 6.5 MB (6547955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91772d23a664a240344cb92a59a93449b1225c12b0db18dfd15540f025e2a7a6`  
		Last Modified: Fri, 24 Jul 2020 16:49:10 GMT  
		Size: 3.6 MB (3580008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
