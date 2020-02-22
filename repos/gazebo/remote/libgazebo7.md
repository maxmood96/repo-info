## `gazebo:libgazebo7`

```console
$ docker pull gazebo@sha256:3a1adde4b4ccecc028dcafb83182b37a14f765cd23014bc3e5b9163ee102f9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo7` - linux; amd64

```console
$ docker pull gazebo@sha256:b3c67851b05829766cfd8f8607d120ac67db38e6146b4ab442621c6c1759cc11
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.9 MB (509912806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b6e8df29fe27d44b599d047052e07e232966162be9676875a04a158b33d7a1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:26:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:26:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 21 Feb 2020 23:26:31 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 21 Feb 2020 23:28:07 GMT
RUN apt-get update && apt-get install -q -y     gazebo7=7.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 23:28:07 GMT
EXPOSE 11345
# Fri, 21 Feb 2020 23:28:07 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 21 Feb 2020 23:28:07 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 21 Feb 2020 23:28:08 GMT
CMD ["gzserver"]
# Fri, 21 Feb 2020 23:30:30 GMT
RUN apt-get update && apt-get install -q -y     libgazebo7-dev=7.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800fbbcfa76fef22becb19160c1bc6ff902d29e48da7cbbf10dc139f88399424`  
		Last Modified: Fri, 21 Feb 2020 23:44:38 GMT  
		Size: 16.7 MB (16656445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d1ccb8bcca00d55e3e0cbaa6ebc7de8c4b3c2cddda85f8ce41d1bc5f365e8b`  
		Last Modified: Fri, 21 Feb 2020 23:44:34 GMT  
		Size: 13.1 KB (13119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6138c22d01789aa9d9feb0ccfacf5f26d9a6e0f27b80d8a49470a5b605853e`  
		Last Modified: Fri, 21 Feb 2020 23:44:34 GMT  
		Size: 5.5 KB (5520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025559e6749872e63f778f6dfef89765e7e18f4bc508633153df0ecc5cb2438`  
		Last Modified: Fri, 21 Feb 2020 23:45:05 GMT  
		Size: 189.8 MB (189780833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75958b52b14f1654a39d50fb5b8f5680e6d54f2d8869a75564d1b41f3ebc7467`  
		Last Modified: Fri, 21 Feb 2020 23:44:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e74814905efa94a834e042cf439bcfa5d708ce3b5c62e9d31f74721ab8678f`  
		Last Modified: Fri, 21 Feb 2020 23:46:05 GMT  
		Size: 259.3 MB (259263429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
