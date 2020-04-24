## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:0dc960973bcac4f95928d8fbe00b413b80b49517fb1af146e9c554f1dda8095c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5ef5e80620b65bc1fb341ca0f15693350d43803f7aa9524403d674588d121a93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38978880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ee761815270f60b72c330300402f8898a72d547271374f22ab157c9b578530`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:46 GMT
ADD file:0ab26fb2f991568d8c593278d4713aed6f3962b7017e3e97e9e3f276031316b2 in / 
# Fri, 20 Mar 2020 19:20:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:49 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:52:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:52:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:767fb6cc1b890aa8046de6d03522b32e23be0de28399261969d00d2666827988`  
		Last Modified: Fri, 20 Mar 2020 19:21:41 GMT  
		Size: 28.5 MB (28521801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c917d9c558a31b32c8cde71574bb4e5f32f55d211e9f0a24345b4b5cbb076dec`  
		Last Modified: Fri, 20 Mar 2020 19:21:37 GMT  
		Size: 31.6 KB (31643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fef7dab626401e4c58516546265cd18118fd3e9258278400e932c811e5d132c`  
		Last Modified: Fri, 20 Mar 2020 19:21:36 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7950fd118d3c2144a9737933f5ba06b35a0f4fab5667001c3f101f87a9cd09`  
		Last Modified: Fri, 20 Mar 2020 19:21:36 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffa145b61007d9318e97209cfefe9ba50ebd86732b5d616bf7778beed1ff0af`  
		Last Modified: Fri, 20 Mar 2020 19:57:49 GMT  
		Size: 6.9 MB (6859499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dec3ed7b85ac54f7c70e2acb445fd9a1c0f4f2d6d9730f689dc16a33f59c4f`  
		Last Modified: Fri, 20 Mar 2020 19:57:48 GMT  
		Size: 3.6 MB (3564924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ad5cb20d5f70fad962d9946dbdd3a289e2237786db446b290a0f0abe48b469a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32774347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2981f6ab820f611a5eb157a18ae9d719cf5a9d7650965520839f3fed0e416247`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jan 2020 01:01:57 GMT
ADD file:2d3ba051ed20fafa578680b18fbe731818ef6ab90ced4b0d6783816de70b6a6f in / 
# Thu, 16 Jan 2020 01:02:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:02:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:02:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:02:38 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:12:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 02:13:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fc4316c8e9493de0b0e1b0cc1c1b9b1fb58750baed7140f2fd1d7d964c601fc3`  
		Last Modified: Thu, 16 Jan 2020 01:05:12 GMT  
		Size: 23.8 MB (23835040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf21553c3db6ce4ac20d8a949658bc8bd42e4658e34d64017f3e117eb6da1c92`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 30.6 KB (30569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2d0679b20cd11ff9c15f051b0c8be2781fdd2237f065c0be6336cfa58d0d9a`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35042469e78e129ca9456d1cd736e5850df94ac632815d85a09777c32fb0082`  
		Last Modified: Thu, 16 Jan 2020 01:05:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5466c47a95ace9c543ced1eb1256ea7b8c427c0c022cca72e8cc24ffbb31f6`  
		Last Modified: Thu, 16 Jan 2020 02:25:43 GMT  
		Size: 5.9 MB (5871813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff48eabde2f5a7ee75934543812cd750a9d08b78244571f77da78f6e588dde`  
		Last Modified: Thu, 16 Jan 2020 02:25:43 GMT  
		Size: 3.0 MB (3035891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed9c12af416d915dc120820658d31316ea718277acfc04ae7a6e9277320bb0fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37423720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f885e7ecac320b3fe4561e23e925ef874080304ebc1fb134bf8b961cbb6bbd25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:44:18 GMT
ADD file:627246f3025f0a9473866d1a3f837c7bc78c1bb64018aefa683ed63fd6b8affd in / 
# Fri, 20 Mar 2020 18:44:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:44:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:44:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:44:25 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:17:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:17:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9806bdadc1314b3e8b4d5249399ac07348da8dfd86b71f450d4a8d5bd672df12`  
		Last Modified: Fri, 20 Mar 2020 18:45:35 GMT  
		Size: 27.1 MB (27127860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a0e1a95f5228adef261b8a421a32e0c6326702c2219757fd4c6ab176ae46d`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08ae661b4f6495649f65df48cfe19cbbaada45e4c46064378e416fe5c68c11`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e5fbabbfbbb4adc0246d014df57f1f8ed76e8f16b7cc3d313a1a7eafe628f7`  
		Last Modified: Fri, 20 Mar 2020 18:45:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da3d88749ec83ebe9d4c864674283cf8c82e033908fe57827b0fa550edadc6`  
		Last Modified: Fri, 20 Mar 2020 19:24:16 GMT  
		Size: 6.7 MB (6722069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4563cf360577e6079155b2b2a1d6538186dd007e8b140dfab33037ed16fd04ea`  
		Last Modified: Fri, 20 Mar 2020 19:24:15 GMT  
		Size: 3.5 MB (3541103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:11986eb1e441bd43fa5136d3a0be216306f2c61c5b99185bbd34023e5fbe1bf8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45498034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3b422a51dd619c41d69101aa82f90e47ba7ee7f162fbc1da48566eb4cd37fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:23:44 GMT
ADD file:aa6837ec5fc9aa5509004c5c2f8d9f4fca19beb57131babb5f3ab770ccb50cd1 in / 
# Fri, 20 Mar 2020 19:23:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:23:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:24:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:24:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:39:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:40:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c60419ce4ad313deb007f5835ca7d2bd045778a693e50b3d2a66ddce1a36e995`  
		Last Modified: Fri, 20 Mar 2020 19:26:06 GMT  
		Size: 33.3 MB (33255285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46f94aa4e6b2f9a3f0e7562389f25dc0ff07b147a0f5e369e09d220dab91a6`  
		Last Modified: Fri, 20 Mar 2020 19:25:59 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95829298b5408a704109b7f54f06ba7180c2088d8b138b4069b0c0b72c989c36`  
		Last Modified: Fri, 20 Mar 2020 19:25:58 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4176ec2142d9c14ab633f5b3939c935d942d3af3ee9de948d70c8ea60146b05e`  
		Last Modified: Fri, 20 Mar 2020 19:25:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa00bbcfb61c4e0f2c416561c35902360fe4e9bf213bd33fe8ae03a6628e07`  
		Last Modified: Fri, 20 Mar 2020 20:54:32 GMT  
		Size: 7.8 MB (7811511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7d10881b5d3005f25cbe0c3d42ce03e8718d006eb0e29bfdeab6cc5c0a6449`  
		Last Modified: Fri, 20 Mar 2020 20:54:31 GMT  
		Size: 4.4 MB (4398695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b64d23e43326f7a5c1177b36e8e892e9e606b357f9c84f4569d32cdd4cae2cef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37414254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c96264f6219c4a2e38127c44e04dc1152afc77d781d45c81957fe7771b9b61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 17:53:14 GMT
ADD file:03baa8497a93a00ea995231d15634436cb152a22e31352725880a4b75b30923b in / 
# Thu, 23 Apr 2020 17:53:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:53:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:53:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:53:26 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:50:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:50:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b89947e6c970275fe5141523cefd56fe22ec68e92d2c52df040e0180499d7325`  
		Last Modified: Thu, 23 Apr 2020 17:54:44 GMT  
		Size: 27.3 MB (27269329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e47f221ce9e120c7fca222f6577fbabdbdb6816775ce618f7dc85359d696e3d`  
		Last Modified: Thu, 23 Apr 2020 17:54:37 GMT  
		Size: 33.0 KB (32958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2393ffdac88d55ee26fed7939dd73c113922d49409bad6eefc5be72e32ea5ddb`  
		Last Modified: Thu, 23 Apr 2020 17:54:37 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb770f5b82ab402fae938a100bf82731f920074dffae67553e29448ae74423b`  
		Last Modified: Thu, 23 Apr 2020 17:54:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c9625da54b32ed8d0fd7eb9dd77426f27c092b7f2c64bd7d837fa2e8f78a17`  
		Last Modified: Fri, 24 Apr 2020 07:56:10 GMT  
		Size: 6.5 MB (6548496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24806be1367361d89d21b7b460d873b0271bdec80b3f3e2d266679b7e854277a`  
		Last Modified: Fri, 24 Apr 2020 07:56:09 GMT  
		Size: 3.6 MB (3562441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
