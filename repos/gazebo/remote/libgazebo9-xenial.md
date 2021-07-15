## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:6f28c114daceb2c1ab55d4ebfc4acbe4e896f8e0b79b4681fa891ea94913873d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:e351e7ab3965d735bc64fd87f12b72ed823f97a1370149deeca0c177f7321bf4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.7 MB (495680415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a908f50e0f9c0f8b2e3d511aa8f76ac5e1763d9ba6504cc9f6b8a8066fe9f4`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
# Fri, 18 Jun 2021 01:17:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:17:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 18 Jun 2021 01:17:25 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 18 Jun 2021 01:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.18.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:20:07 GMT
EXPOSE 11345
# Fri, 18 Jun 2021 01:20:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 18 Jun 2021 01:20:07 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 18 Jun 2021 01:20:07 GMT
CMD ["gzserver"]
# Fri, 18 Jun 2021 01:22:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.18.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cddf96b1d9077906b30f50e138b6a3252ffd88b232b089e83fe44a7bd6c7ee`  
		Last Modified: Fri, 18 Jun 2021 01:25:10 GMT  
		Size: 16.3 MB (16280641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da236e19087ee88e3d53dc8684ebad98a87d090cdfa20b0664d1ef075a90ad85`  
		Last Modified: Fri, 18 Jun 2021 01:25:07 GMT  
		Size: 14.8 KB (14760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e3219184ae4a068c37d17466fa31e4b668da0a8aa1aab644332242d1568727`  
		Last Modified: Fri, 18 Jun 2021 01:25:07 GMT  
		Size: 5.5 KB (5548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f7b72e048f6f06f857c6451f33db681d0df8c07c0175197ebbab25e0ce1082`  
		Last Modified: Fri, 18 Jun 2021 01:25:32 GMT  
		Size: 208.1 MB (208107236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88be717ab0f0ac9523f01087fe7aa20e14037760e1eef54805acf9b8f722895a`  
		Last Modified: Fri, 18 Jun 2021 01:25:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a191dbc1d07f0183233b725f609ec0c732369d214b5f9b2586de6dd775d40c`  
		Last Modified: Fri, 18 Jun 2021 01:26:18 GMT  
		Size: 224.8 MB (224773711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
