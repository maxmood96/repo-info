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
$ docker pull gazebo@sha256:46011861a6a5625f8d92d1065f475ad4dde8b0b2e4ae60e47cb43f0715a2e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver10` - linux; amd64

```console
$ docker pull gazebo@sha256:160013464a51bf58b80cf261a7f39b43b34178eebb705b0d208733b47722062b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268411671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9184ad444546c2a677edbcf7034eb685d47e92707143061a79fdd1b2aca59834`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:32:27 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:32:27 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:32:27 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:32:27 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21335bed604914a59b8bb98c108397862d9129e67e5586aae00c1d6fc108b056`  
		Last Modified: Thu, 17 Sep 2020 00:49:09 GMT  
		Size: 226.2 MB (226170170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61a323dba166733ea5e65464a1da1e370b3170f244bdc89a1a0d7cf8554a20`  
		Last Modified: Thu, 17 Sep 2020 00:48:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver10-bionic`

```console
$ docker pull gazebo@sha256:46011861a6a5625f8d92d1065f475ad4dde8b0b2e4ae60e47cb43f0715a2e4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver10-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:160013464a51bf58b80cf261a7f39b43b34178eebb705b0d208733b47722062b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268411671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9184ad444546c2a677edbcf7034eb685d47e92707143061a79fdd1b2aca59834`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:32:27 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:32:27 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:32:27 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:32:27 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21335bed604914a59b8bb98c108397862d9129e67e5586aae00c1d6fc108b056`  
		Last Modified: Thu, 17 Sep 2020 00:49:09 GMT  
		Size: 226.2 MB (226170170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61a323dba166733ea5e65464a1da1e370b3170f244bdc89a1a0d7cf8554a20`  
		Last Modified: Thu, 17 Sep 2020 00:48:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:a0a81cbddee6c7b22c12e1767fae1177946efe1583d1eade0ea534fe453f0a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:0425b11ed0e5b1b985e3a4e2c4cc40e2f3234e1e6fed82446ff820783e19aed3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313385004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14ac4838333896cec396a181e8fc4534eeda30930310428e9d56999cfeabc20`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:37:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:39:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:39:54 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:39:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:39:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:39:54 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33f64348e3aebaf209bae28143ea09b3f91809a9a065e265e58169a5c984bba`  
		Last Modified: Thu, 17 Sep 2020 00:52:15 GMT  
		Size: 16.1 MB (16116699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9057c528555b86c79f685c3af20edc72dedbdaee4dd9bb03f3a9c47f6b1f6f1`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e14ecfe86c07e223655174eb28581bdf3fb8b3d2e41e0a3bbbd8d73cdb34401`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 5.5 KB (5468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f49d5f8649e4aaba0e3678f287fa2dd061610f1b737cbdbbfb7e66f4016d1`  
		Last Modified: Thu, 17 Sep 2020 00:52:52 GMT  
		Size: 267.5 MB (267526596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ab50886b2437d974b2617da2fc3d90a3af1ed09bae1061d0683528c40f6dd3`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:8230e16196c8beb61c692f614de355b229066571b20d668df5411397c7c73fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:939b913b539392c60f1ea2b6a7f1f5b37f937fcf69ab7a1323b21bc46a0bbff3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (276997909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d86ab0519debd1d299eb2ee124fb0fc66bbfafa09431e1fd61b594d04e86400`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:35:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:35:15 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:35:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:35:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:35:16 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee96d9670934bc75bce3539cd01c0fab3e8dd140f23471f1f3d9d381a8710526`  
		Last Modified: Thu, 17 Sep 2020 00:50:57 GMT  
		Size: 234.8 MB (234756408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8fc72423b5b140fe0ab28c59ee029741237a028fb31cc6dbdca1ead1a13c5`  
		Last Modified: Thu, 17 Sep 2020 00:50:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:a0a81cbddee6c7b22c12e1767fae1177946efe1583d1eade0ea534fe453f0a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:0425b11ed0e5b1b985e3a4e2c4cc40e2f3234e1e6fed82446ff820783e19aed3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313385004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14ac4838333896cec396a181e8fc4534eeda30930310428e9d56999cfeabc20`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:37:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:39:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:39:54 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:39:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:39:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:39:54 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33f64348e3aebaf209bae28143ea09b3f91809a9a065e265e58169a5c984bba`  
		Last Modified: Thu, 17 Sep 2020 00:52:15 GMT  
		Size: 16.1 MB (16116699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9057c528555b86c79f685c3af20edc72dedbdaee4dd9bb03f3a9c47f6b1f6f1`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e14ecfe86c07e223655174eb28581bdf3fb8b3d2e41e0a3bbbd8d73cdb34401`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 5.5 KB (5468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f49d5f8649e4aaba0e3678f287fa2dd061610f1b737cbdbbfb7e66f4016d1`  
		Last Modified: Thu, 17 Sep 2020 00:52:52 GMT  
		Size: 267.5 MB (267526596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ab50886b2437d974b2617da2fc3d90a3af1ed09bae1061d0683528c40f6dd3`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver7`

```console
$ docker pull gazebo@sha256:d4bb1351df9ca266258c57d092cb578a43240b487c8175177c72d40f33c91222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver7` - linux; amd64

```console
$ docker pull gazebo@sha256:3e9d4181af226a8e046b203b63bd31ac7429742cfc4ac325d90da12d7134a047
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242424081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498be094fedf75dfaf9bd008736019d2fee99977e00b003e319363179d7f7b97`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:22:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:22:01 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:22:02 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:22:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:22:02 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ef38e9401109365596af8828ae7e9d9af506b5ff583b5873e267ea43b1780d`  
		Last Modified: Thu, 17 Sep 2020 00:44:22 GMT  
		Size: 181.6 MB (181636131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa14dd9f226b37ede587989373891badada90544df0dd15200bfcd5c18ea359d`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver7-xenial`

```console
$ docker pull gazebo@sha256:d4bb1351df9ca266258c57d092cb578a43240b487c8175177c72d40f33c91222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver7-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:3e9d4181af226a8e046b203b63bd31ac7429742cfc4ac325d90da12d7134a047
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242424081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498be094fedf75dfaf9bd008736019d2fee99977e00b003e319363179d7f7b97`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:22:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:22:01 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:22:02 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:22:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:22:02 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ef38e9401109365596af8828ae7e9d9af506b5ff583b5873e267ea43b1780d`  
		Last Modified: Thu, 17 Sep 2020 00:44:22 GMT  
		Size: 181.6 MB (181636131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa14dd9f226b37ede587989373891badada90544df0dd15200bfcd5c18ea359d`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:72bc9052b3455262c56b910c681a22f9bde8ca36c490ee16eaca720ddd0ce7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:a87782acfb2a22ee7e2180390d97590566763c5199885dc4d3bda3779e30abc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268458118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e7d779ba595d74bb5e4273eb15b7bb623da7e24dd994d16f9a31f482b1491`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:29:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:29:07 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:29:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:29:07 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:29:07 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2b1122402285c04bddbb55ecff09902422df1a1ea98db9df5b532a07098d3d`  
		Last Modified: Thu, 17 Sep 2020 00:47:28 GMT  
		Size: 226.2 MB (226216616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6613cbfeaf2f24c28c5f770620c9bd2a35d070bf0e49e7ca094885187070cdb`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-bionic`

```console
$ docker pull gazebo@sha256:72bc9052b3455262c56b910c681a22f9bde8ca36c490ee16eaca720ddd0ce7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:a87782acfb2a22ee7e2180390d97590566763c5199885dc4d3bda3779e30abc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268458118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579e7d779ba595d74bb5e4273eb15b7bb623da7e24dd994d16f9a31f482b1491`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:29:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:29:07 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:29:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:29:07 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:29:07 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2b1122402285c04bddbb55ecff09902422df1a1ea98db9df5b532a07098d3d`  
		Last Modified: Thu, 17 Sep 2020 00:47:28 GMT  
		Size: 226.2 MB (226216616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6613cbfeaf2f24c28c5f770620c9bd2a35d070bf0e49e7ca094885187070cdb`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:ed3abb45296162f3e9f01b17aa9332834f5bec3e830584acb29e70ff6fc38c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:3e003070f91adc4ee1e1784d3798008a29ad41c3276e2dacb955301ad919bfbb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265958745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0563d59b0956698c1b80e4b884ab41216ccd2b93a9a279171d77e0df83fb7688`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 05:40:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 05:40:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 10 Sep 2020 05:40:29 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 10 Sep 2020 05:41:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 05:41:31 GMT
EXPOSE 11345
# Thu, 10 Sep 2020 05:41:32 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 10 Sep 2020 05:41:32 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 10 Sep 2020 05:41:32 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dcc12496391485e9809615cfcd2938af53d7c813909bf3a4e27b71aaa81633`  
		Last Modified: Thu, 10 Sep 2020 05:44:30 GMT  
		Size: 18.5 MB (18515141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50266b329110929cbbaaed679354348702002842555979a900e8efb4ad8d8a10`  
		Last Modified: Thu, 10 Sep 2020 05:44:22 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b81a9923ffb06a1aeea39dd3de22d7c9b36ab43604fa91fb71a2213651a02`  
		Last Modified: Thu, 10 Sep 2020 05:44:22 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f14d12dfa8ee0385ac5c6f3d71ddeb6ba5fe158248c4237b838f402eda8c61`  
		Last Modified: Thu, 10 Sep 2020 05:45:02 GMT  
		Size: 202.1 MB (202070285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e655cb9e364ff32c993c304d598310a8a335e4259e147d967f6ac2d309b162fb`  
		Last Modified: Thu, 10 Sep 2020 05:44:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-xenial`

```console
$ docker pull gazebo@sha256:0412cee182096d8e9900ea01fbee22749ed885ec1d3120c0087123c04d1a4e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:7d23632752eb0d1a5f5fdcd4a6994dd0f7ce3081201da757c96514889b0c45a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269029711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2109d787479456df884b00231e82698241ba2822f429b4202ae07b20c23b1f9`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:25:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:25:20 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:25:20 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:25:20 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:25:20 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e205af1b54a73e841f21db3e7959a57e565068a91207e99bd0c2f4fa6c0e08`  
		Last Modified: Thu, 17 Sep 2020 00:45:53 GMT  
		Size: 208.2 MB (208241759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764ae8b7716bc1ea237bcb6e5d1b353df1f8ab62c8ea7752bf994665450ef6de`  
		Last Modified: Thu, 17 Sep 2020 00:45:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:latest`

```console
$ docker pull gazebo@sha256:19221cc0d8839504d43e361fc1c7b500b8f28af6bbe25e68d513a80af3bd3ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:490f7525d170cf93d749a8dc22f2ccd1eafd4c694c94cd999af9052a6ac0ed1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 MB (589990324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a0e8c0b32ac7d8a4129c0b6f853125539373aec41172318353b2d146068548`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:37:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:39:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:39:54 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:39:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:39:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:39:54 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:43:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo11-dev=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33f64348e3aebaf209bae28143ea09b3f91809a9a065e265e58169a5c984bba`  
		Last Modified: Thu, 17 Sep 2020 00:52:15 GMT  
		Size: 16.1 MB (16116699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9057c528555b86c79f685c3af20edc72dedbdaee4dd9bb03f3a9c47f6b1f6f1`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e14ecfe86c07e223655174eb28581bdf3fb8b3d2e41e0a3bbbd8d73cdb34401`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 5.5 KB (5468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f49d5f8649e4aaba0e3678f287fa2dd061610f1b737cbdbbfb7e66f4016d1`  
		Last Modified: Thu, 17 Sep 2020 00:52:52 GMT  
		Size: 267.5 MB (267526596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ab50886b2437d974b2617da2fc3d90a3af1ed09bae1061d0683528c40f6dd3`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2837810cacfa3034766eef5d69e1ebe325fb8e4d707e0f9b8389d5c0bb5c82`  
		Last Modified: Thu, 17 Sep 2020 00:54:12 GMT  
		Size: 276.6 MB (276605320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo10`

```console
$ docker pull gazebo@sha256:670cb4165de6b46ad25dc7d6f49407afac94da53f79cff897861e3369b252d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo10` - linux; amd64

```console
$ docker pull gazebo@sha256:022862c84c1e3310c7339f5b3fa4b6ec9ae835550570944aab601b260eb870ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522039346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28cbb63829d8e6606295feef7ab84bb05c13931aa137549f8716adab4a28997`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:32:27 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:32:27 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:32:27 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:32:27 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:34:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo10-dev=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21335bed604914a59b8bb98c108397862d9129e67e5586aae00c1d6fc108b056`  
		Last Modified: Thu, 17 Sep 2020 00:49:09 GMT  
		Size: 226.2 MB (226170170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61a323dba166733ea5e65464a1da1e370b3170f244bdc89a1a0d7cf8554a20`  
		Last Modified: Thu, 17 Sep 2020 00:48:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9c4f3088467aedf58e9b364049dcd17f487b153409c4acd80025d42be25c9`  
		Last Modified: Thu, 17 Sep 2020 00:50:07 GMT  
		Size: 253.6 MB (253627675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo10-bionic`

```console
$ docker pull gazebo@sha256:670cb4165de6b46ad25dc7d6f49407afac94da53f79cff897861e3369b252d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo10-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:022862c84c1e3310c7339f5b3fa4b6ec9ae835550570944aab601b260eb870ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.0 MB (522039346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28cbb63829d8e6606295feef7ab84bb05c13931aa137549f8716adab4a28997`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:32:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:32:27 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:32:27 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:32:27 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:32:27 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:34:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo10-dev=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21335bed604914a59b8bb98c108397862d9129e67e5586aae00c1d6fc108b056`  
		Last Modified: Thu, 17 Sep 2020 00:49:09 GMT  
		Size: 226.2 MB (226170170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61a323dba166733ea5e65464a1da1e370b3170f244bdc89a1a0d7cf8554a20`  
		Last Modified: Thu, 17 Sep 2020 00:48:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa9c4f3088467aedf58e9b364049dcd17f487b153409c4acd80025d42be25c9`  
		Last Modified: Thu, 17 Sep 2020 00:50:07 GMT  
		Size: 253.6 MB (253627675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:19221cc0d8839504d43e361fc1c7b500b8f28af6bbe25e68d513a80af3bd3ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:490f7525d170cf93d749a8dc22f2ccd1eafd4c694c94cd999af9052a6ac0ed1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 MB (589990324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a0e8c0b32ac7d8a4129c0b6f853125539373aec41172318353b2d146068548`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:37:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:39:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:39:54 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:39:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:39:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:39:54 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:43:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo11-dev=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33f64348e3aebaf209bae28143ea09b3f91809a9a065e265e58169a5c984bba`  
		Last Modified: Thu, 17 Sep 2020 00:52:15 GMT  
		Size: 16.1 MB (16116699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9057c528555b86c79f685c3af20edc72dedbdaee4dd9bb03f3a9c47f6b1f6f1`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e14ecfe86c07e223655174eb28581bdf3fb8b3d2e41e0a3bbbd8d73cdb34401`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 5.5 KB (5468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f49d5f8649e4aaba0e3678f287fa2dd061610f1b737cbdbbfb7e66f4016d1`  
		Last Modified: Thu, 17 Sep 2020 00:52:52 GMT  
		Size: 267.5 MB (267526596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ab50886b2437d974b2617da2fc3d90a3af1ed09bae1061d0683528c40f6dd3`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2837810cacfa3034766eef5d69e1ebe325fb8e4d707e0f9b8389d5c0bb5c82`  
		Last Modified: Thu, 17 Sep 2020 00:54:12 GMT  
		Size: 276.6 MB (276605320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:a3a02eba9bdd48e510136f363350b6f4042bee78a7cc0a1be3d4281f1ede5cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:b171c37b98d55544eee3845235e1e6d83eb6997de1493e3146ede0c2f3029c87
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542835580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a4b222d8f900adccaac677d6051e711afb19e9f8d30e90b8b8b9c0f625ed70`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:35:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:35:15 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:35:15 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:35:15 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:35:16 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:36:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo11-dev=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee96d9670934bc75bce3539cd01c0fab3e8dd140f23471f1f3d9d381a8710526`  
		Last Modified: Thu, 17 Sep 2020 00:50:57 GMT  
		Size: 234.8 MB (234756408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d8fc72423b5b140fe0ab28c59ee029741237a028fb31cc6dbdca1ead1a13c5`  
		Last Modified: Thu, 17 Sep 2020 00:50:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cd8dca5670b71599def541b1cce8e27eef755bc8d0bbb96212ea954b5bb70f`  
		Last Modified: Thu, 17 Sep 2020 00:51:58 GMT  
		Size: 265.8 MB (265837671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:19221cc0d8839504d43e361fc1c7b500b8f28af6bbe25e68d513a80af3bd3ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:490f7525d170cf93d749a8dc22f2ccd1eafd4c694c94cd999af9052a6ac0ed1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 MB (589990324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a0e8c0b32ac7d8a4129c0b6f853125539373aec41172318353b2d146068548`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:37:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:37:28 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:39:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo11=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:39:54 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:39:54 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:39:54 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:39:54 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:43:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo11-dev=11.1.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33f64348e3aebaf209bae28143ea09b3f91809a9a065e265e58169a5c984bba`  
		Last Modified: Thu, 17 Sep 2020 00:52:15 GMT  
		Size: 16.1 MB (16116699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9057c528555b86c79f685c3af20edc72dedbdaee4dd9bb03f3a9c47f6b1f6f1`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e14ecfe86c07e223655174eb28581bdf3fb8b3d2e41e0a3bbbd8d73cdb34401`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 5.5 KB (5468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f49d5f8649e4aaba0e3678f287fa2dd061610f1b737cbdbbfb7e66f4016d1`  
		Last Modified: Thu, 17 Sep 2020 00:52:52 GMT  
		Size: 267.5 MB (267526596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ab50886b2437d974b2617da2fc3d90a3af1ed09bae1061d0683528c40f6dd3`  
		Last Modified: Thu, 17 Sep 2020 00:52:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2837810cacfa3034766eef5d69e1ebe325fb8e4d707e0f9b8389d5c0bb5c82`  
		Last Modified: Thu, 17 Sep 2020 00:54:12 GMT  
		Size: 276.6 MB (276605320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo7`

```console
$ docker pull gazebo@sha256:ae79c9debc417b013ebc113d881aa56bb488728653bb672890deb6070b3dde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo7` - linux; amd64

```console
$ docker pull gazebo@sha256:b0fafa8e91ed8af3772fe61861403e4be1cafb47b4a512cc86f0bdccb08b15a0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482840274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ee0dfbe8c180f8bedf4c1f21e65bcf8d0a5d8c43c2a6717e63f77c39d47fce`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:22:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:22:01 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:22:02 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:22:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:22:02 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:24:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo7-dev=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ef38e9401109365596af8828ae7e9d9af506b5ff583b5873e267ea43b1780d`  
		Last Modified: Thu, 17 Sep 2020 00:44:22 GMT  
		Size: 181.6 MB (181636131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa14dd9f226b37ede587989373891badada90544df0dd15200bfcd5c18ea359d`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ab0250b87fc490d2cafa048d683db9a5d87c0f691d530bb68764c17c1b7a2`  
		Last Modified: Thu, 17 Sep 2020 00:45:18 GMT  
		Size: 240.4 MB (240416193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo7-xenial`

```console
$ docker pull gazebo@sha256:ae79c9debc417b013ebc113d881aa56bb488728653bb672890deb6070b3dde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo7-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:b0fafa8e91ed8af3772fe61861403e4be1cafb47b4a512cc86f0bdccb08b15a0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482840274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ee0dfbe8c180f8bedf4c1f21e65bcf8d0a5d8c43c2a6717e63f77c39d47fce`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:22:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo7=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:22:01 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:22:02 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:22:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:22:02 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:24:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo7-dev=7.16.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ef38e9401109365596af8828ae7e9d9af506b5ff583b5873e267ea43b1780d`  
		Last Modified: Thu, 17 Sep 2020 00:44:22 GMT  
		Size: 181.6 MB (181636131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa14dd9f226b37ede587989373891badada90544df0dd15200bfcd5c18ea359d`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ab0250b87fc490d2cafa048d683db9a5d87c0f691d530bb68764c17c1b7a2`  
		Last Modified: Thu, 17 Sep 2020 00:45:18 GMT  
		Size: 240.4 MB (240416193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9`

```console
$ docker pull gazebo@sha256:d53509059f6c2b2b3c22ba923db64dfbc79023b6892bae775982df35eb87c8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9` - linux; amd64

```console
$ docker pull gazebo@sha256:0e3f186126d588333f0b570b37584e936fed27abacd23ea3fc597f0aafcddd31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413573985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d94720584d3853d2536ba5c7c598052ee74a99ee8e9cce41c858aac84ab5fb`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:29:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:29:07 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:29:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:29:07 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:29:07 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:31:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo9-dev=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2b1122402285c04bddbb55ecff09902422df1a1ea98db9df5b532a07098d3d`  
		Last Modified: Thu, 17 Sep 2020 00:47:28 GMT  
		Size: 226.2 MB (226216616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6613cbfeaf2f24c28c5f770620c9bd2a35d070bf0e49e7ca094885187070cdb`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6401314411d4c615b7803de295348aeb03e9484084636151285901cb411953`  
		Last Modified: Thu, 17 Sep 2020 00:48:13 GMT  
		Size: 145.1 MB (145115867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:d53509059f6c2b2b3c22ba923db64dfbc79023b6892bae775982df35eb87c8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:0e3f186126d588333f0b570b37584e936fed27abacd23ea3fc597f0aafcddd31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413573985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d94720584d3853d2536ba5c7c598052ee74a99ee8e9cce41c858aac84ab5fb`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:26:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:26:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:27:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:27:06 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:29:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:29:07 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:29:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:29:07 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:29:07 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:31:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo9-dev=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5aab880c2f23fd5bf095a6e1a941ba3c3488993cfc6ee5357ef112834aa0f0e`  
		Last Modified: Thu, 17 Sep 2020 00:46:55 GMT  
		Size: 838.2 KB (838176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e78bd72568b169672f452c20b3e119fd68e8f73c0979f2b94d80d7bc4e7df3`  
		Last Modified: Thu, 17 Sep 2020 00:46:57 GMT  
		Size: 14.7 MB (14695638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc0b1433be0fe7a435a2b915a49069e0f9e5de7218dae315369d5cb37981076`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e1672ac8a128d7cb77e2ef9e7f2c1e71b47c019c9adfa7b3d1b39e10a530`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 5.4 KB (5435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2b1122402285c04bddbb55ecff09902422df1a1ea98db9df5b532a07098d3d`  
		Last Modified: Thu, 17 Sep 2020 00:47:28 GMT  
		Size: 226.2 MB (226216616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6613cbfeaf2f24c28c5f770620c9bd2a35d070bf0e49e7ca094885187070cdb`  
		Last Modified: Thu, 17 Sep 2020 00:46:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6401314411d4c615b7803de295348aeb03e9484084636151285901cb411953`  
		Last Modified: Thu, 17 Sep 2020 00:48:13 GMT  
		Size: 145.1 MB (145115867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:6d6372f3586e3d32ff5f192c1fd38eb215e8ecf281adbd2821e8886a6ffedd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:090ff736c1d4d3cc65fdc7b1a6b88ff406453787616aaf6b38fbcdbb0903a336
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.9 MB (569882453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219fb259696f5eb81eae5a858b581a889c4b6748b7014522d4b02ee55fc7cdb2`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:04 GMT
ADD file:d8d46fb9e0436b304449f4155e3b1a86d8fdfd809364286726e5b33746db53c0 in / 
# Thu, 10 Sep 2020 00:30:05 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 05:40:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 05:40:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 10 Sep 2020 05:40:29 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 10 Sep 2020 05:41:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 05:41:31 GMT
EXPOSE 11345
# Thu, 10 Sep 2020 05:41:32 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 10 Sep 2020 05:41:32 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 10 Sep 2020 05:41:32 GMT
CMD ["gzserver"]
# Thu, 10 Sep 2020 05:43:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo9-dev=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f250268ed6a0b777b9a3d9e0659754a8c97f28420f30cb78c184c3eead07d14`  
		Last Modified: Thu, 10 Sep 2020 00:37:25 GMT  
		Size: 45.4 MB (45366726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dcc12496391485e9809615cfcd2938af53d7c813909bf3a4e27b71aaa81633`  
		Last Modified: Thu, 10 Sep 2020 05:44:30 GMT  
		Size: 18.5 MB (18515141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50266b329110929cbbaaed679354348702002842555979a900e8efb4ad8d8a10`  
		Last Modified: Thu, 10 Sep 2020 05:44:22 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261b81a9923ffb06a1aeea39dd3de22d7c9b36ab43604fa91fb71a2213651a02`  
		Last Modified: Thu, 10 Sep 2020 05:44:22 GMT  
		Size: 5.0 KB (4984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f14d12dfa8ee0385ac5c6f3d71ddeb6ba5fe158248c4237b838f402eda8c61`  
		Last Modified: Thu, 10 Sep 2020 05:45:02 GMT  
		Size: 202.1 MB (202070285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e655cb9e364ff32c993c304d598310a8a335e4259e147d967f6ac2d309b162fb`  
		Last Modified: Thu, 10 Sep 2020 05:44:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affeed96611110e679292558872ce45c2df9be416ea147b838d17418c8ad9f80`  
		Last Modified: Thu, 10 Sep 2020 05:46:12 GMT  
		Size: 303.9 MB (303923708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:649bdf9541303e2c317932c90238383bce3fc58ba27f28afb8afa51b5b2bb91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:4ad80845f11d2ad24947d9bb9e904cd725cfdff1b116fccace5fb1a447392a69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.7 MB (493706514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6ce5effdd5a1a9f48a262b3b36733dba954f68c273d4b5b54433f208ef9f00`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 16 Sep 2020 22:22:41 GMT
ADD file:22e6fa4e90b4c26ba962a4fe57e5784d8923885e6eb39435cb121c716c42f7ff in / 
# Wed, 16 Sep 2020 22:22:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:22:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 22:22:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:22:44 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:20:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:20:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 17 Sep 2020 00:20:38 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 17 Sep 2020 00:25:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:25:20 GMT
EXPOSE 11345
# Thu, 17 Sep 2020 00:25:20 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 17 Sep 2020 00:25:20 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 17 Sep 2020 00:25:20 GMT
CMD ["gzserver"]
# Thu, 17 Sep 2020 00:26:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     libgazebo9-dev=9.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:001ecc9468da6632359722ccefa732463486659ee07daacd31602ec3bf4d862f`  
		Last Modified: Fri, 04 Sep 2020 13:20:12 GMT  
		Size: 44.5 MB (44490811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9667498691604756cf3601ba44360f2b1f6ba8b5745eee963847d2a4ea736`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe474042557a4bffb655cd6079656d79e2ecfb0d0fad367c610ca1ec65d0e86`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf2fb0fbbc55e614a3391455d772eae373e0136b7cba4d79dd72f28fb347f0`  
		Last Modified: Wed, 16 Sep 2020 22:23:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23745095fc5b866fe80a41a9d827fc0027d0e564830927fd45f206f89e43b8ba`  
		Last Modified: Thu, 17 Sep 2020 00:44:01 GMT  
		Size: 16.3 MB (16275124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd51ea5fe22dbe02f8b46c4c532caa3b0a7756e08f06a32671044099e35246b`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941ee3cbf738a5bb24ce28dcd138850f496d80ac791aaf7772b102417b54729`  
		Last Modified: Thu, 17 Sep 2020 00:43:53 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e205af1b54a73e841f21db3e7959a57e565068a91207e99bd0c2f4fa6c0e08`  
		Last Modified: Thu, 17 Sep 2020 00:45:53 GMT  
		Size: 208.2 MB (208241759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764ae8b7716bc1ea237bcb6e5d1b353df1f8ab62c8ea7752bf994665450ef6de`  
		Last Modified: Thu, 17 Sep 2020 00:45:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c187f6fdac217055cbfe648d68aecaf4d42113fa801ff784625406569821782`  
		Last Modified: Thu, 17 Sep 2020 00:46:50 GMT  
		Size: 224.7 MB (224676803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
