## `gazebo:libgazebo10`

```console
$ docker pull gazebo@sha256:8751c4b27b8dcac3e527bd9bbf310b2eba2c7ebf99f34131dcf47d6ead1271ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo10` - linux; amd64

```console
$ docker pull gazebo@sha256:69f1c245ba9b246a3ff9aa0eea3612fbb62b3247531fcaaec347813fb02f2e70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 MB (522102075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4b85f43f36f96233f3df9fe3cc2cd617d1718fa3c7fdfc4e3b469898dec410`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:01:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Thu, 04 Mar 2021 04:01:54 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Thu, 04 Mar 2021 04:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo10=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:06:48 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:06:48 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:06:48 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:06:48 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:08:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo10-dev=10.2.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b94d68aa12dd4301ba7129ecb94e0239755427abab911c3c2da85ec660198`  
		Last Modified: Thu, 04 Mar 2021 04:18:21 GMT  
		Size: 14.7 MB (14700028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e22c583b48c8061e09530c65be6ab8d653600c47d6e62c97959e420c203cc4`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a328364513ce50172ca27eae2734f0f1fd7561ecb73f4b1ed44417a5fa476fa`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 5.4 KB (5436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6a32c4f72367f5709d855a46f4a5ee39df84e1e4267a9a5c7ced3e793ac23`  
		Last Modified: Thu, 04 Mar 2021 04:20:18 GMT  
		Size: 226.2 MB (226227727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91743264d4edbe70a25141d36e0449fe212318c7bed42bd54b3a48822f15b9f`  
		Last Modified: Thu, 04 Mar 2021 04:19:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c315bde239facfcacabbf6edb55f2b4b1ea994cf83d72aeb4e2d6c42a9cf00`  
		Last Modified: Thu, 04 Mar 2021 04:21:10 GMT  
		Size: 253.6 MB (253614796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
