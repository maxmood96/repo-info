## `buildpack-deps:hirsute-curl`

```console
$ docker pull buildpack-deps@sha256:f367a0a81086c4228686c72f380293116e01bcb2b2a056c35fd7ae9d897b9cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v7

### `buildpack-deps:hirsute-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8203901a80e30a1b3699110ca0f97c8f5816d07cc637fdac061ffafbde4b49e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34313963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267114c3e108462739c1732d3c4ccd132d6787cbacb3d4706123c43c81eca938`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 23:00:24 GMT
ADD file:efa60bd7da49bad0a724434362f77d98c9f3c786170c7fef64ecb57aa808b18e in / 
# Wed, 25 Nov 2020 23:00:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 23:00:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 23:00:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 23:00:31 GMT
CMD ["/bin/bash"]
# Thu, 17 Dec 2020 08:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:41:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cf5d8cf40e57262478b56493eaf1bb9d9a8ecde1d37cfc10e81f73798a0a5b7a`  
		Last Modified: Mon, 23 Nov 2020 22:54:17 GMT  
		Size: 26.3 MB (26336795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d0e651346be2ec39fb01f211210fa42a2ec5212300b3a6d73f450dd1dc709d`  
		Last Modified: Wed, 25 Nov 2020 23:02:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe721ee3adfabbef45101e3cdd00ff12aa4ea18319502279b4da2389a2c153f`  
		Last Modified: Wed, 25 Nov 2020 23:02:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6b39ed7adb6a7a6d999508a6ae30fe04c7a403accfe529f05acf9a5e742833`  
		Last Modified: Thu, 17 Dec 2020 09:01:48 GMT  
		Size: 4.8 MB (4849916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9e63643887e8142d918de418503ee33102967776ae4dcda5389138288430ec`  
		Last Modified: Thu, 17 Dec 2020 09:01:48 GMT  
		Size: 3.1 MB (3126212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
