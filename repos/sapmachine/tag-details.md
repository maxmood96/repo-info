<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.6.0.1`](#sapmachine110601)
-	[`sapmachine:14`](#sapmachine14)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:8b7b21e8a1e09e55aaa6e1c0b5cfed13fcd4d91460ae34b5560868d3ead87b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:22db588d0f4616efa95e982ceaa063c02e79ae1538b6b948c397f3659de95c51
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231533967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce40e0c48d0f3dd488cc08eb3221a9d7f887d5e25e88da35f00c54a98794d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:12:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:45:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.6.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:45:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 20 Mar 2020 03:45:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199d1ee7a365d83b69a7e0e652aebcfac19a91e8bf339b89067950c8dcf6fb6e`  
		Last Modified: Sat, 22 Feb 2020 01:13:48 GMT  
		Size: 7.6 MB (7564366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabea60f665705bcb863ecfa728b76926f489f6847e137a3afbecad48cf84613`  
		Last Modified: Fri, 20 Mar 2020 03:46:54 GMT  
		Size: 197.2 MB (197241125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.6.0.1`

```console
$ docker pull sapmachine@sha256:8b7b21e8a1e09e55aaa6e1c0b5cfed13fcd4d91460ae34b5560868d3ead87b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sapmachine:11.0.6.0.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:22db588d0f4616efa95e982ceaa063c02e79ae1538b6b948c397f3659de95c51
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231533967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce40e0c48d0f3dd488cc08eb3221a9d7f887d5e25e88da35f00c54a98794d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:12:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:45:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.6.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:45:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 20 Mar 2020 03:45:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199d1ee7a365d83b69a7e0e652aebcfac19a91e8bf339b89067950c8dcf6fb6e`  
		Last Modified: Sat, 22 Feb 2020 01:13:48 GMT  
		Size: 7.6 MB (7564366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabea60f665705bcb863ecfa728b76926f489f6847e137a3afbecad48cf84613`  
		Last Modified: Fri, 20 Mar 2020 03:46:54 GMT  
		Size: 197.2 MB (197241125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:14`

```console
$ docker pull sapmachine@sha256:31dbef00903e3f7970ff07a971e9f2925beab13a6ab4a5c60a5cc3e63e564683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sapmachine:14` - linux; amd64

```console
$ docker pull sapmachine@sha256:e7dc62555f3152eb2913899ecef71789a8230af540839169543da99db2b481c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246940254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bb4db83d43a6707f94c89eb5d83f607b0601fb797e2080272069b9bbd0008a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:08 GMT
ADD file:6c8f103b672b6dc8b10903d40d33227d3b7a8e8df1af80e47142523f2b849adf in / 
# Thu, 16 Jan 2020 01:21:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:21:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:10 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 03:45:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:46:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-14-jdk=14     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:46:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-14
# Fri, 20 Mar 2020 03:46:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f6b7df711c8a4733138390ff2aba1bfeb755bf4736c39c6e4858076c40fb5eb`  
		Last Modified: Thu, 16 Jan 2020 01:22:19 GMT  
		Size: 28.4 MB (28363102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0703c52b8763604318dcbb1730c82ad276a487335ecabde2f43f69a6222e8090`  
		Last Modified: Thu, 16 Jan 2020 01:22:15 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07304348ce1b6d24f136a3c4ebaa800297b804937a6942ce9e9fe0dac0b0ca74`  
		Last Modified: Thu, 16 Jan 2020 01:22:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795dceb8869bdfa64f3742e1df492e6f31baf9cfc36f1a042a8f981607e99a2`  
		Last Modified: Thu, 16 Jan 2020 01:22:15 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac7ffd6f3c7e08a91b555609371f736598a5d8896d5e2b18971bc1936674b7`  
		Last Modified: Fri, 20 Mar 2020 03:47:13 GMT  
		Size: 8.5 MB (8548037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534759ab6b46b94735be86f5755bc25b7972b9cc4c2959b4ecd4b0e99bd82fb4`  
		Last Modified: Fri, 20 Mar 2020 03:47:31 GMT  
		Size: 210.0 MB (209997499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:31dbef00903e3f7970ff07a971e9f2925beab13a6ab4a5c60a5cc3e63e564683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:e7dc62555f3152eb2913899ecef71789a8230af540839169543da99db2b481c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246940254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bb4db83d43a6707f94c89eb5d83f607b0601fb797e2080272069b9bbd0008a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:08 GMT
ADD file:6c8f103b672b6dc8b10903d40d33227d3b7a8e8df1af80e47142523f2b849adf in / 
# Thu, 16 Jan 2020 01:21:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:21:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:10 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 03:45:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:46:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-14-jdk=14     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:46:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-14
# Fri, 20 Mar 2020 03:46:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f6b7df711c8a4733138390ff2aba1bfeb755bf4736c39c6e4858076c40fb5eb`  
		Last Modified: Thu, 16 Jan 2020 01:22:19 GMT  
		Size: 28.4 MB (28363102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0703c52b8763604318dcbb1730c82ad276a487335ecabde2f43f69a6222e8090`  
		Last Modified: Thu, 16 Jan 2020 01:22:15 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07304348ce1b6d24f136a3c4ebaa800297b804937a6942ce9e9fe0dac0b0ca74`  
		Last Modified: Thu, 16 Jan 2020 01:22:14 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4795dceb8869bdfa64f3742e1df492e6f31baf9cfc36f1a042a8f981607e99a2`  
		Last Modified: Thu, 16 Jan 2020 01:22:15 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac7ffd6f3c7e08a91b555609371f736598a5d8896d5e2b18971bc1936674b7`  
		Last Modified: Fri, 20 Mar 2020 03:47:13 GMT  
		Size: 8.5 MB (8548037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534759ab6b46b94735be86f5755bc25b7972b9cc4c2959b4ecd4b0e99bd82fb4`  
		Last Modified: Fri, 20 Mar 2020 03:47:31 GMT  
		Size: 210.0 MB (209997499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:8b7b21e8a1e09e55aaa6e1c0b5cfed13fcd4d91460ae34b5560868d3ead87b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:22db588d0f4616efa95e982ceaa063c02e79ae1538b6b948c397f3659de95c51
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231533967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce40e0c48d0f3dd488cc08eb3221a9d7f887d5e25e88da35f00c54a98794d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:12:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:45:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.6.0.1     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 03:45:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 20 Mar 2020 03:45:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199d1ee7a365d83b69a7e0e652aebcfac19a91e8bf339b89067950c8dcf6fb6e`  
		Last Modified: Sat, 22 Feb 2020 01:13:48 GMT  
		Size: 7.6 MB (7564366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabea60f665705bcb863ecfa728b76926f489f6847e137a3afbecad48cf84613`  
		Last Modified: Fri, 20 Mar 2020 03:46:54 GMT  
		Size: 197.2 MB (197241125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
