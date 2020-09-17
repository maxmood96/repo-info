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
