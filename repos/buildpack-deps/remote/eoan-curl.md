## `buildpack-deps:eoan-curl`

```console
$ docker pull buildpack-deps@sha256:79b0f0946f72df3623795bc3f18e18c8a1e9ba778a47e4cbe7eab1a11221660b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:eoan-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2e6a264e93732821f5eacc0efb7fef5dffd0384625508def4ad0dd34d1708b50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38337308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29d3ab5a88f575d3a078e803823e6961ba6aadf01e0ce57fc3d89a0631126bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:34 GMT
ADD file:537f9883fb90d19383082b8ac20c17b581db9045a48fa28b83cab73fe317047d in / 
# Fri, 20 Mar 2020 19:20:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:36 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:48:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:eeacba527962683a1b026af611fe162d35281159762b699172caa48c69480f79`  
		Last Modified: Mon, 16 Mar 2020 15:44:17 GMT  
		Size: 28.3 MB (28276050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25405ed4f245fc5627d0b03996d04c11d492c7a9ff937f4562a18e8757c39434`  
		Last Modified: Fri, 20 Mar 2020 19:21:27 GMT  
		Size: 30.6 KB (30632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22752cd61bd53e9ac71e22fef539c165b3e11b368c1e54ca947260e317c4870a`  
		Last Modified: Fri, 20 Mar 2020 19:21:27 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460de83957c509dd234ede9ea96d4d03b7f9cd252ef1497844f8450dedb6570`  
		Last Modified: Fri, 20 Mar 2020 19:21:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42eb88f91904b1b4337337103ab96430c87f3ad2e37d3f822b84a655bd0809e`  
		Last Modified: Fri, 20 Mar 2020 19:57:01 GMT  
		Size: 6.5 MB (6512597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ff84c2324c65af66e83971227b34dc08eb47fa329d526af15e72ee7c2243b8`  
		Last Modified: Fri, 20 Mar 2020 19:57:00 GMT  
		Size: 3.5 MB (3517022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6ebe01c4e45709e77b552960fea4a9e9e7f68fafe801138934b1f5474242b8d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32282238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928dbef9bf075f0402464b85d375a8d69a40eb5f973f82ff010aeeb5b0ab16fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:58:53 GMT
ADD file:d5ea94843f1a1e0976b02f8e02c5256c148157dd51f492da5181ad8753622ab4 in / 
# Fri, 20 Mar 2020 18:58:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:58:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:58:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:58:59 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:21:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:21:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ea86edd9db57be0bd75bed151c49e031bd6699fcbd94130c3a8a8ab459692de`  
		Last Modified: Mon, 16 Mar 2020 15:44:38 GMT  
		Size: 23.7 MB (23735633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6c62210e628371fc8ed38017e5360a6a15489b56acd8dba096dc79768da4ca`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 30.6 KB (30613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325644a644873d31f1108862c1ed632f57c3fbc43ebe7603f57c2c0d39a3665`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c4a05bf433715cda695415ab43dfdcae3e89606057e6ab273703fa768f4a6d`  
		Last Modified: Fri, 20 Mar 2020 19:00:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5329b380082dac433270a0b1ad42ffe176511a6b4a4a7f6081c725d8a9772858`  
		Last Modified: Fri, 20 Mar 2020 19:26:53 GMT  
		Size: 5.5 MB (5532315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02e6dbd45902d44e8810a3b6e246f1b3b62a3b0345c64c711bba978777b0d6`  
		Last Modified: Fri, 20 Mar 2020 19:26:53 GMT  
		Size: 3.0 MB (2982641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f422fc721b7d3c3b18b444a1e1a6e451280d6af20c42d64566197ebe3e99611b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36783227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08eb8bf2d1400d844f0ccdc17bb2163aba5ea310ca74d64804e4fc2212e2e91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:43:59 GMT
ADD file:908424aa468cb2a7000dd795511259c67a0f70d0bbafa4b05b405faf89be8a02 in / 
# Fri, 20 Mar 2020 18:44:01 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:44:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:44:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:44:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:14:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:14:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:20fe7914fb520387e59fda29e21ea64541bf9e7e95c9eef77a6ac68c18d23349`  
		Last Modified: Mon, 16 Mar 2020 15:44:48 GMT  
		Size: 26.9 MB (26869532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c6aa3850fcf8c6207823b79f1560303443a33d4fe996bf809b4dc7d00f7d35`  
		Last Modified: Fri, 20 Mar 2020 18:45:14 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ac1bb4168bfb44e13693f63bd600c9230216a2443e5fb4839aedbb31635a2`  
		Last Modified: Fri, 20 Mar 2020 18:45:14 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b98aacf49712db6881b4d4da724b4349964afa1b6e6b4e983b7465c028513`  
		Last Modified: Fri, 20 Mar 2020 18:45:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87bce95c870b3e429de8b2891d6e9fd55ff65194bb2c98b4dd1517d810be1ed`  
		Last Modified: Fri, 20 Mar 2020 19:23:03 GMT  
		Size: 6.4 MB (6370756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420f2437c57580d01b2aecf81116f84e3120a5062815f6ea05b18bac2f74e9f8`  
		Last Modified: Fri, 20 Mar 2020 19:23:02 GMT  
		Size: 3.5 MB (3511455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6054ccae28b784653e39ed9047085a854eb3332ceeea2c4f3fd00e2a18f00be0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39727339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f603fe55e61ffb8772bcf703b5191170de4b2b765487f6f14db9af7a6e311ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 21:17:15 GMT
ADD file:f7ba0a72b1867680590e06dee4957489f61064444c99136216e872289753205b in / 
# Thu, 23 Apr 2020 21:17:16 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 21:17:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 21:17:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 21:17:18 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 09:05:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 09:05:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fcc600edb6cfd0f1f659b23300df5716d9534682f7bb847b2cf3fa623aa90a31`  
		Last Modified: Mon, 13 Apr 2020 15:44:55 GMT  
		Size: 29.0 MB (29044041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d3ca6655399bfe2c1ed6e5a5456d1d666e48dc9ed14da2a0cbb347933ab0ef`  
		Last Modified: Thu, 23 Apr 2020 21:18:04 GMT  
		Size: 30.7 KB (30696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7cdb9cb7ad5cdc2e1cc3e791d3dc33d99ce8079b4924664bc77a8af0dfcf38`  
		Last Modified: Thu, 23 Apr 2020 21:18:04 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec81ba1924129679b6fcec1e55d28a6d71fbcfbe7db715aea9ef144c50ac6d`  
		Last Modified: Thu, 23 Apr 2020 21:18:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a766ccdbe901ed5e2ffa8521e25dc52dc93157673fc3e64f66e7770118c4cc`  
		Last Modified: Fri, 24 Apr 2020 09:14:04 GMT  
		Size: 6.8 MB (6841269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48044873d3301355963c44fdfdcaafe8cec317eb1e7d10fb4cc46e4a8d8199e`  
		Last Modified: Fri, 24 Apr 2020 09:14:04 GMT  
		Size: 3.8 MB (3810325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e582f55c1fa59809a3b4e1ddade5af100346974b0303d66bedc86d06b384a59e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44901983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e11fe6860f95983a44728f9f95844d46f669eadf297169dc907e6462230d2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:23:08 GMT
ADD file:5f2d0c54e4b302f16104b557b94863ea583b0f5077cdba4a739077166e742286 in / 
# Fri, 20 Mar 2020 19:23:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:23:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:23:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:23:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:26:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:26:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ed545fde3a421d26f2fe47bd4ffaa6f5e4d1922ee226f849b9030af8e0469cb6`  
		Last Modified: Mon, 16 Mar 2020 15:46:10 GMT  
		Size: 33.0 MB (32986715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dc90382a97787ce60215cad11117e850fe8c74a63cb5b8ce024645ea62b7a8`  
		Last Modified: Fri, 20 Mar 2020 19:25:21 GMT  
		Size: 30.5 KB (30494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c59e83ff7085e57aab1e4c48a50af629cf66f6ae0c896c7ca190d951b38b1f1`  
		Last Modified: Fri, 20 Mar 2020 19:25:21 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6ff0efafd163296380421cd94ed46d501335204734c716873fde2954ae4d84`  
		Last Modified: Fri, 20 Mar 2020 19:25:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b12250d905cd2b3af1ed612fbcd1792c072d94aa5bb27f5ad3a94aed436c3`  
		Last Modified: Fri, 20 Mar 2020 20:53:06 GMT  
		Size: 7.4 MB (7420572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866515692221b069b60e0e16398694fe3e3ab0a294b549f3c6b3b55f4ffe0835`  
		Last Modified: Fri, 20 Mar 2020 20:53:07 GMT  
		Size: 4.5 MB (4463169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:eoan-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:54f282009099c9a4c7fde2d93a8a066f05a4ec03951f6b5cff27c76f70aadaab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36288087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340bb60537454a1cb269b2cdf5c61e1601ea595324495dd3a65d52a68f3579cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:44 GMT
ADD file:590238292f6a053ea2bf6e08f583c7d381c15ead1a8a0f1bad600fca48d20648 in / 
# Thu, 23 Apr 2020 17:52:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:56 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:49:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:49:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4a7e39a0b3f9ba3421a213b5b6ae19b4ee4315b5aff0252496ef8117c7caae2e`  
		Last Modified: Mon, 13 Apr 2020 15:45:44 GMT  
		Size: 26.7 MB (26682562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15519bbe785a81349f4b9318ec98f07fb1d7ed9742eaf004a27806254935f5bf`  
		Last Modified: Thu, 23 Apr 2020 17:54:25 GMT  
		Size: 31.1 KB (31106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a183d313a7aec756ef4cec9ebed83e7eefb892c64f68a74fb640abde8a647`  
		Last Modified: Thu, 23 Apr 2020 17:54:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0914614caf2827873d1d4b1f12426334285b8d984af44e48b64b7db18c3ee4fc`  
		Last Modified: Thu, 23 Apr 2020 17:54:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba99f74f403727ed8ce2e6a910248a0a53edf2bff04fe4fe7551ee0acbaaf849`  
		Last Modified: Fri, 24 Apr 2020 07:55:26 GMT  
		Size: 6.1 MB (6139662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7833d62efa3405cf0f7f73e663802e5167b8fe4fc84628bdc4e14a161891379`  
		Last Modified: Fri, 24 Apr 2020 07:55:26 GMT  
		Size: 3.4 MB (3433720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
