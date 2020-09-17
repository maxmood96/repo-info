## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:37e08142bb4f00f71a3a6d18f1145c0ee3c3f261e4de188ba816b796a3eb21e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:edd4ff8530b010fd97c0fea3e0ab2e75efa781744407901708f13fa8fdada55a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94347768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad6ed20d953179393bce4e34f2ab7567248c7ae538797bd2ce53f94c65c73b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:21:20 GMT
ADD file:b31229f77879183d5bdbe48d32b3ecdfe46410dec50c588d6af01768ffdbd794 in / 
# Wed, 16 Sep 2020 22:21:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:21:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:21:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:21:22 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:10:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Sep 2020 00:10:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2777c0a13c374e25addf3c52f9a1133e1fd4a1d19dc208565fb5efd20677e52`  
		Last Modified: Mon, 14 Sep 2020 15:54:43 GMT  
		Size: 28.8 MB (28828512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b6e79464f24063f1012cda557cbf24d8e5c52705e8c78c5dd154522516fff`  
		Last Modified: Wed, 16 Sep 2020 22:23:20 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c493930b10bd8d1999cfa2ac8c524fd771f991c4f944f58d47477050ff0af92`  
		Last Modified: Wed, 16 Sep 2020 22:23:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ce40c7ec243f304ee5a7eb659c8cb2980a80b46d3626b4bb7104a6c3115b40`  
		Last Modified: Thu, 17 Sep 2020 00:18:28 GMT  
		Size: 6.9 MB (6916964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b21e42016855267240c03118951556272910ac92e8b4178f2c34c31ce72d6bf`  
		Last Modified: Thu, 17 Sep 2020 00:18:27 GMT  
		Size: 3.6 MB (3586222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb3476409ea2eb730d6dc80161441d9258f409c67dfca2e09f19fdae5186e1e`  
		Last Modified: Thu, 17 Sep 2020 00:18:42 GMT  
		Size: 55.0 MB (55015060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ecc92cfd42bb2fc2bfeeabd4ff84937c238cae1a25d83416b60686ae9bb784e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83063077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439693e63f342ca255468b4ea73f3f93804cbb9c9dc852ab3a6dca9934ca2499`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:29:17 GMT
ADD file:5d040dcb9ecf5ea37a47528d7671364427c6db8500998cdd61b0d6197561327f in / 
# Wed, 16 Sep 2020 22:29:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:29:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:29:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:29:25 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:09:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:09:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Sep 2020 23:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fc3824011019fe6b44b5748af8b7264a274c0a308a19877b49366eca72e87c6f`  
		Last Modified: Mon, 14 Sep 2020 15:55:44 GMT  
		Size: 24.2 MB (24215640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6d99a2cc8e2dba749dca1fa6342625fb00d84d872023ff24b63cf05de7e300`  
		Last Modified: Wed, 16 Sep 2020 22:31:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31de15bc5097b24b529945a61185eddf0085a7c414695486a452ae14bbf76441`  
		Last Modified: Wed, 16 Sep 2020 22:31:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df75cbfcf2f91455215a85704a6718af9f113389d440c9945cf4a364a2b7e84f`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 5.9 MB (5900389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da3018ef17ec885a89b88f73ffa69e4d81da2be4a4f3fc6e94eea3ce96e4f03`  
		Last Modified: Wed, 16 Sep 2020 23:18:37 GMT  
		Size: 3.1 MB (3059076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4f4563acb0571e477217543b72004e2084f79ad41f4e1a6ea0391056b724c4`  
		Last Modified: Wed, 16 Sep 2020 23:19:03 GMT  
		Size: 49.9 MB (49886934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6f6c6270afc3aa576c7d03b7672f06a0fc6acb93077486443e3cc4e2c19b810d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92837399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a49e1ea924081abf70734ae0c8cd2018dfde07af37c83374548d59fc36f1ce8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:17:16 GMT
ADD file:49c6724d85a07ca6b5b6275cb112749b5cbfdcbfe61415086380e74078bc8671 in / 
# Wed, 16 Sep 2020 23:17:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:17:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:17:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:17:24 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:18:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:18:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Sep 2020 00:19:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:819fdbd74ad8047dc411b4e024934bdffa3e92b0927c37d008a60e16264997b1`  
		Last Modified: Mon, 14 Sep 2020 15:55:20 GMT  
		Size: 27.4 MB (27435541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78ef2e809f83cf7858d674a77fce1cc2cd088601ef9b601c8c52b62c2917596`  
		Last Modified: Wed, 16 Sep 2020 23:18:55 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e47e504262a6132624edf51d3fb1c94306b2502df33e27fcdcb67a6335e44f5`  
		Last Modified: Wed, 16 Sep 2020 23:18:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f02c68adf7f957e8499517272ca54cbc8359a3013f1f4dbb33ca5c83b28159d`  
		Last Modified: Thu, 17 Sep 2020 00:27:58 GMT  
		Size: 6.8 MB (6781918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c15f1213e09b07654719720543d612c8324246e32587cbfb6155a9d18294e3`  
		Last Modified: Thu, 17 Sep 2020 00:27:57 GMT  
		Size: 3.6 MB (3570554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af319e3f8b4a70a982d0fe0fe78b264e05cb47e6c6e86b9391d529e7102a5629`  
		Last Modified: Thu, 17 Sep 2020 00:28:24 GMT  
		Size: 55.0 MB (55048348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:34fc3a3495a7ff8a15d4b459a63c6483ecd1efd3fff60609ffaf202727807e52
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109161545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701a1f5cdfc6c53cefb236bd347a775688a9c77695119fd6768d8ed74863c6ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:10 GMT
ADD file:d2bdf56089aa739c01f4fea190a17051fbcd45e31fa5ba26d466921d4b528a06 in / 
# Wed, 19 Aug 2020 21:16:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:16:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:49 GMT
CMD ["/bin/bash"]
# Thu, 20 Aug 2020 00:32:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:33:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 20 Aug 2020 00:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd233d33322880c9108ff9d4a2836417f422f1f76cea04cbce12861b48e4ec0a`  
		Last Modified: Mon, 17 Aug 2020 15:54:01 GMT  
		Size: 33.5 MB (33521520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948f26d4116ec9c2f8ce7b5d3765e3f977e8e62da7b636f40f1d3d554b6027e3`  
		Last Modified: Wed, 19 Aug 2020 21:19:34 GMT  
		Size: 30.9 KB (30877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2568d3b37f18de7a6f08771049d897ef5d8bdbf2ddba783262fee3d781a2c588`  
		Last Modified: Wed, 19 Aug 2020 21:19:33 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271de21485d292cc9b05d3b055184c64751e0cf915de5be7c595ef973f80d104`  
		Last Modified: Wed, 19 Aug 2020 21:19:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e242cd3731e0ee7c6107fbde83668bf7dbbc2f329278aa64548b8b6e69ca1e`  
		Last Modified: Thu, 20 Aug 2020 01:06:16 GMT  
		Size: 7.8 MB (7816668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0357a04a0eaa3f73a4e0de3317b10e7b6ee2cff741c22e8b4cd78cab3c8d0b77`  
		Last Modified: Thu, 20 Aug 2020 01:06:15 GMT  
		Size: 4.4 MB (4446779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acf10fdc3db810bf8d904b3a9bf00377f86aa5ac5f0f7a7705f15edc031154`  
		Last Modified: Thu, 20 Aug 2020 01:06:41 GMT  
		Size: 63.3 MB (63344665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4bb143f925bc1b33b563f777c771fb0f407f75cf387d63203e129e0b497c8c83
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94268782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a447583931026cf8ce46529091b080d643e5d022a9f785aaf9e70efd3693af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:51:52 GMT
ADD file:8b60e925c7d1fc58aa03cec6200d56eb171cec4d8856766d062a02d6a9d35045 in / 
# Wed, 16 Sep 2020 22:51:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:51:55 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:51:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:51:56 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:27:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Sep 2020 23:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:526c3f0b06221923628388a7879c5dca9ad737704d8a5bb52f62eccb945d9eea`  
		Last Modified: Mon, 14 Sep 2020 15:56:09 GMT  
		Size: 28.7 MB (28685212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145f5fb5761ec5efa6c7cb81f5dc235263a5a2f9e47211b8f15246e0cb57e2ec`  
		Last Modified: Wed, 16 Sep 2020 22:52:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b29e60d7164662b93f8c1f52116015aa2b25b569943a2e639e113d24636e45`  
		Last Modified: Wed, 16 Sep 2020 22:52:44 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2f1d47f5fe9d42008269fa4e79252c02f5f254b095022a8fae3d641d3cb82b`  
		Last Modified: Wed, 16 Sep 2020 23:32:36 GMT  
		Size: 6.8 MB (6815484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaad1df7e2e32fe332a0cb661fc000f23fc4e690bc709af6adc5c7b1bf48f57`  
		Last Modified: Wed, 16 Sep 2020 23:32:35 GMT  
		Size: 3.6 MB (3579356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41544c86e4dc24fbcf1c8586679a1d4d2a42fae5f691150b130b62e7e425e974`  
		Last Modified: Wed, 16 Sep 2020 23:32:50 GMT  
		Size: 55.2 MB (55187694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
