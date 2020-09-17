## `buildpack-deps:groovy-curl`

```console
$ docker pull buildpack-deps@sha256:24481b0d8c9f31d71fda631bc8cc08b4043d60ff030a240debc87bd821395a34
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
$ docker pull buildpack-deps@sha256:a4ca0bad61c73f7223d8d4912a052b2fe2f8fa0533f96e1ae4f5f2ab552ac0e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12710f432bf291f52c377396452d5874b2d3593d68acc89923b794f7ecceeafd`
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

### `buildpack-deps:groovy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c31289befb0df49110470a9df9388e4f28177487ba6d0e437717b95c19f059c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33176143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bec91d1724f09a42bb3ea2d5e4778518aa902ccefef2828cefad498bafd3194`
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

### `buildpack-deps:groovy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0ace326b44a65bb3a4117ade0ec705888f3a9d4ff6b3df7a1c5aa6e6197f4b61
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37789051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dd39f8fd6fbe9b39c32aaad954fc96dc0c9451b7ec38d0cc5df56d792100c8`
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
$ docker pull buildpack-deps@sha256:334c1315a250412970ffc34b1bb1bc662ea37dd7aa063cdf422bb3fae66c4110
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39081088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5a759df3141af3855bc2d6e0baf02e47064839c303b9af47fc94dc67c9b960`
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
