## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:005915c864239ee907582f70e8240345dde11eaca541e547346c00fef709caa3
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
$ docker pull buildpack-deps@sha256:bcb4662ca8ff2b0464560e51abd61d8179d0eeb294fdcbcf35ebe99913a0ac9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39447039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4425d8adbad5f920128000d507bc11f38524861d957092e59aa0da2f7e92e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:34:53 GMT
ADD file:d74bec7765901e52fa9fac8c6c45b3246a5becce64a39f1f6b27a918febdd435 in / 
# Fri, 25 Sep 2020 22:34:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:34:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:34:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:34:55 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:31:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:31:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5cb735c93c49ccc75005489c239a41732c3fba617b5efd9db967f1ab8387063a`  
		Last Modified: Mon, 21 Sep 2020 15:55:50 GMT  
		Size: 31.3 MB (31341151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7431e3c410bb05888131d9f68d2100a319c7e89892e6dab17c0dccc06143fe52`  
		Last Modified: Fri, 25 Sep 2020 22:37:10 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb7a4dd012f7f05e95ddda6864c3a38097244f292a40d6b36cd3ed87d0909f1`  
		Last Modified: Fri, 25 Sep 2020 22:37:10 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db575a0596bb2fe176de3f751b2924451bdef2ffbf40736fdeb95555c95c448`  
		Last Modified: Fri, 25 Sep 2020 23:39:23 GMT  
		Size: 4.5 MB (4515848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b15bd04a0ae103f36375c57920dab82817f08fa67f3c3917060aa01fc5101b3`  
		Last Modified: Fri, 25 Sep 2020 23:39:23 GMT  
		Size: 3.6 MB (3589032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c0a0e1b1c250aa603bf9104ef865e1a08c3ea80d275a9817a8fe6fa945c6f7f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33343431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41414facbf94e572b34bb91f2ee08d7d4c180654a8db8aeccbd89536cbeec913`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 23:05:28 GMT
ADD file:70774dfd3e8f26aee57a3cbc4a6b73c0dd4052690db73b7770c4b17c06b9a871 in / 
# Fri, 25 Sep 2020 23:05:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:05:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:05:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:05:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 01:11:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 01:11:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5d952dc4eb5ddd4c1f4cb9e992e88b82906c1a2eb036b22a366fc3002110d961`  
		Last Modified: Mon, 21 Sep 2020 15:56:41 GMT  
		Size: 26.3 MB (26326996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e1292d20f334d084ab39cee0036c3244df6b6b323d6a1f925878f2dbf6a4b`  
		Last Modified: Fri, 25 Sep 2020 23:07:06 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7daf62c539de75bdeecd1a84790d0d330d7dbeb1cd413c12c7e5ebde618fee5`  
		Last Modified: Fri, 25 Sep 2020 23:07:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55322016d95f300e880eaf359c32e72d0ade7ad4788811cc83de959ab070c13`  
		Last Modified: Sat, 26 Sep 2020 01:21:09 GMT  
		Size: 4.0 MB (3953397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f647204ea56fc16d41a4a3aaec60f6d536e035b87f0f95b4933210e1c256d179`  
		Last Modified: Sat, 26 Sep 2020 01:21:08 GMT  
		Size: 3.1 MB (3062000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b285a01198725b877243fe5b019aa0ae8aa907e531878a5970d8dc739ee3cdb2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37977891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843791e728fdc00b93e7038550ebafe797192ee90354f72e869eaccfd8e9b48f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:48:20 GMT
ADD file:19e0988decae946be321d38e1d62b1d0077df9658b46c0bf1bddca41c3b494eb in / 
# Fri, 25 Sep 2020 22:48:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:48:25 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:48:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:48:27 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:46:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:46:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a3499d851fed144aa7b8a557c949fd67873ce344a4c28fc4a5584c707e51bdec`  
		Last Modified: Mon, 21 Sep 2020 15:56:18 GMT  
		Size: 29.9 MB (29910024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac61158bc63daa8c43df54a85b23e347b8f5ac2bdc79386a8fa37995880d0d`  
		Last Modified: Fri, 25 Sep 2020 22:49:49 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efec76ef326a6718cd323554778f8be1997181aacc1518a81000d6f1fbc92f03`  
		Last Modified: Fri, 25 Sep 2020 22:49:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c50be5bbdbbe352904af627647ce41ba34f5ceb49df99123b918123e013157`  
		Last Modified: Fri, 25 Sep 2020 23:56:35 GMT  
		Size: 4.5 MB (4493222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fec50125567814e59bb72444ac2bf2d68ca690637bb765f97d0cb86974bc69`  
		Last Modified: Fri, 25 Sep 2020 23:56:36 GMT  
		Size: 3.6 MB (3573612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c2080f8884add5b4dbd31f535b2185f927e9222326956ca872b64351c0588bef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45901393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174412d7e0fc3cf6c71284bdb2763a722fa70ae3db81c5f17e075c82796558cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:56:53 GMT
ADD file:af607e950dc0b0e0569c00abeafa5cb60aab1276650394154ee00b9362d76a5a in / 
# Wed, 16 Sep 2020 23:57:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:57:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:57:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:57:39 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 03:27:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 03:28:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:154f672fc406f14b4f51d017ded4bedbe66d9c63d039e8225eefaf7a4b06b031`  
		Last Modified: Mon, 14 Sep 2020 15:55:59 GMT  
		Size: 33.6 MB (33573385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64504423517eebb592d091d4e0de5c37b82ec58fe8eb7c44ee8f8c05b16d9f14`  
		Last Modified: Thu, 17 Sep 2020 00:02:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2ce187057b397f7db9db98d75136c8feb5c945207daee696f485f0bb775c12`  
		Last Modified: Thu, 17 Sep 2020 00:02:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32251dafb18e359a8a5ed27e5a16b693fc346f2824d043f51a0d4989d712b49e`  
		Last Modified: Thu, 17 Sep 2020 03:58:07 GMT  
		Size: 7.9 MB (7880299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b198656f1001c1a3580f6205106c51fd05f53a928e2958862f2e96cdb40141`  
		Last Modified: Thu, 17 Sep 2020 03:58:07 GMT  
		Size: 4.4 MB (4446670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e915f726f8ccf1fc0f126d2965d493ad1ade88a62db10e4023e2ffaad29dcb2f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39478741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd71354267849c349ad71a2c20421890ee29a5716bff27d14e2e8ea39799f06a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Sep 2020 22:45:17 GMT
ADD file:89492d6e96925fde151f47721bb76d3d3497e248deebfcd8470c53e9b16a8037 in / 
# Fri, 25 Sep 2020 22:45:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:45:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:45:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:45:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:22:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:22:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b91259bd471bf4c457bc7a08c109ddb2d7e96dd9a3c2a2fe6efbf8fb94cfbda1`  
		Last Modified: Mon, 21 Sep 2020 15:57:23 GMT  
		Size: 31.2 MB (31186236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f77b06dfaa40a67e6b37fcec76245eebcdecaf6b93a73c88f74352b36294417`  
		Last Modified: Fri, 25 Sep 2020 22:46:10 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e47b5b6ebe06b0c93b79e3350cfba27d0ef79386c2859df93ba66c8083e28`  
		Last Modified: Fri, 25 Sep 2020 22:46:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452def7cd68695a7e737dc1860047132f164c6de0fb09b2cd1fb0f40f2bebe58`  
		Last Modified: Fri, 25 Sep 2020 23:26:52 GMT  
		Size: 4.7 MB (4709178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ffc553793ba56a9a6403e2cac0dde3c1428211510febadc0a6f28b0000b8b7`  
		Last Modified: Fri, 25 Sep 2020 23:26:52 GMT  
		Size: 3.6 MB (3582294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
