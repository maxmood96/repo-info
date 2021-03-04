## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:dafb7ca592502af281b79ccce279ab087f019970b8c333dc729b9b2c1a5bcbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:12311b0bcea6ed5b204c940421527653b4a1a0d0dfa6b6f4aad585637c99ae32
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.8 MB (413800086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338aa1c8898fd9de2cfcb2146d82f8aa96c8afadaa800b2f2c86a0c80ffe8a11`
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
# Thu, 04 Mar 2021 04:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:52 GMT
EXPOSE 11345
# Thu, 04 Mar 2021 04:03:52 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Thu, 04 Mar 2021 04:03:52 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Thu, 04 Mar 2021 04:03:53 GMT
CMD ["gzserver"]
# Thu, 04 Mar 2021 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:fd2c851523c97e4363b92141c4aa336d7b84ebf59db5d10d5cdf44c10660e64b`  
		Last Modified: Thu, 04 Mar 2021 04:18:52 GMT  
		Size: 226.3 MB (226341103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38115e1f11af59104be8cea9e0b86f261892fc3f3213eea3ee0828c0d2ac9b0`  
		Last Modified: Thu, 04 Mar 2021 04:18:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94064730068f263fa2c869a8b75607e2296958f0fd8af7f8bd1601f81460839`  
		Last Modified: Thu, 04 Mar 2021 04:19:35 GMT  
		Size: 145.2 MB (145199431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
