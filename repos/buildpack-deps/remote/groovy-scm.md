## `buildpack-deps:groovy-scm`

```console
$ docker pull buildpack-deps@sha256:817512fb53c93512c1667d424bb0701f677bf21587a86eb6305aaa87ac4cbb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le

### `buildpack-deps:groovy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:355ea5cb04d9b4cc63c19c3c23d2b04ef036c1cfb73ec57bcddb544e1e9f52ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101850900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8961be70e1b12bb66e4417638df636cbc150b57bd7cbaec01a4017ec832d264`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 18:42:49 GMT
ADD file:0a4786f61369ab8311ad73df0425a325cc7095cd1d2a955a27c759d6e77320b9 in / 
# Wed, 06 May 2020 18:42:49 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 18:42:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 18:42:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 18:42:51 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:21:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 11 May 2020 18:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4278c4af5b59c968c977e7ebe9d86416b17eb5328985758690e3d3eac8aaa3f4`  
		Last Modified: Wed, 06 May 2020 16:10:34 GMT  
		Size: 28.2 MB (28171554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05b16b3cc63a06490c0e17d7ce09fb81e50884605c98e94db4883e63d9de811`  
		Last Modified: Wed, 06 May 2020 18:43:26 GMT  
		Size: 31.8 KB (31801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3e637c5311a8a3018cf95f210e8f2a56ee3d14c6bbae422d6349d7b93c466e`  
		Last Modified: Wed, 06 May 2020 18:43:25 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2eb2835f6239dd2e96e96b24f169df777bafb9ad56d18129da631d47d0d1a62`  
		Last Modified: Wed, 06 May 2020 18:43:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcd31e5147b6e6e3e0bc52a304cbc500bfca7c1f2eb804b29f376b9fee98148`  
		Last Modified: Mon, 11 May 2020 18:25:36 GMT  
		Size: 6.9 MB (6859390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae361abb991a333032309434504cb932f8c23f767ee99a2cf2dca31ad0a5c66f`  
		Last Modified: Mon, 11 May 2020 18:25:35 GMT  
		Size: 3.8 MB (3801124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c6ebf940958fd34abcaa57540c221c18bb78bbbf7175bd0f5930f2421eca4f`  
		Last Modified: Mon, 11 May 2020 18:25:52 GMT  
		Size: 63.0 MB (62986024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4df19e61851bf20f3ae0b1742e2ebc583ae49318130c08d8df7ff46c7dd470ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117305836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8a76444ecb1c09d72b93c1310300375afb472c262f7dbca2d1fe9064bfa871`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 18:53:34 GMT
ADD file:38bef3b89ab78f35a240c77d3bfd2424cfe83a3bf6c80a86755d0757378faac3 in / 
# Wed, 06 May 2020 18:53:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 18:53:46 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 18:53:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 18:53:53 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:20:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:20:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 11 May 2020 18:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4b677207667f6a9c31fb95628b1688e43185c1e68507b8ce69c6f753fa6ba0b`  
		Last Modified: Wed, 06 May 2020 18:55:08 GMT  
		Size: 32.8 MB (32830571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a7e3233f42ddeee42ce7307c2f23c2e22479c24ac6391bebc3673d1acedd3e`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 31.6 KB (31614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f21b6f278fbf61dc1503c0ae1118b76024acb128bddbbd2588268e7b0649f91`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a08354d087a0cd2da0584d4775ad4cd0dc224a90d08ba7bdb69f3617e83688e`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9641d94e47a948c31373f5d11e71cf0507deb3964f344b8bdb7f49293f8aeb`  
		Last Modified: Mon, 11 May 2020 18:33:19 GMT  
		Size: 7.8 MB (7813663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a3e6208b1cfd7270677514d1f2db85afab8cf34dfb830c72dd011bd388c59`  
		Last Modified: Mon, 11 May 2020 18:33:18 GMT  
		Size: 4.7 MB (4701080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22253cdb40902ecc0b1f5770fd187606bf265971c911aa33a44804223204708f`  
		Last Modified: Mon, 11 May 2020 18:34:41 GMT  
		Size: 71.9 MB (71927870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
