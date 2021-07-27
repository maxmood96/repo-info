## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:dd5962f7cf8e6cf6a750ecba2bd13eecb45af94a6647346ce65a61a16a5c68b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:59259f6b15b307bb81e6372844533cedafbd04683002148f12d1f92151ba5412
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.7 MB (495681540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be89a0df13af2aae167c8f8130516325dd26311e686e4e92eaeb6a2a193430b2`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Mon, 26 Jul 2021 23:31:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:31:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Mon, 26 Jul 2021 23:31:57 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Mon, 26 Jul 2021 23:34:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.18.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:34:51 GMT
EXPOSE 11345
# Mon, 26 Jul 2021 23:34:51 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Mon, 26 Jul 2021 23:34:51 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 26 Jul 2021 23:34:51 GMT
CMD ["gzserver"]
# Mon, 26 Jul 2021 23:37:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.18.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c4f542d04ec9d618714cccb2753ff6005108e6716d042e9ba90b0fb1abc88e`  
		Last Modified: Mon, 26 Jul 2021 23:59:15 GMT  
		Size: 16.3 MB (16281091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd21d450f65b0e32105070b9d3fdcdfb9674c4adfcf1b9d5cf8de28bbc14a8ac`  
		Last Modified: Mon, 26 Jul 2021 23:59:12 GMT  
		Size: 14.8 KB (14758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5db40177bc2e7edc2f24d5b6fd143d881b6c4c37b3345fe19229344628a654`  
		Last Modified: Mon, 26 Jul 2021 23:59:12 GMT  
		Size: 5.5 KB (5549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d43bbb44025f4b6bb6a24d0ddac2ba17150501d366804feca7e11700598e07`  
		Last Modified: Mon, 26 Jul 2021 23:59:36 GMT  
		Size: 208.1 MB (208108078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f620279d9814638866098221cb9783bc7b21d82eb0406520fbb52e4e748794`  
		Last Modified: Mon, 26 Jul 2021 23:59:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34888dcb0d6f62335782ab8df5cdf278b868562a639452bfa11a96e7b8d58992`  
		Last Modified: Tue, 27 Jul 2021 00:00:19 GMT  
		Size: 224.8 MB (224772962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
