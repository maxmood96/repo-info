## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:55c0002859011fad05a8a2aadc3156bfa58922df2819174619a8da0e3f21aae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:9b8ca6c874e474c9031ac64299fb4247623459bf2ac7187fd3509632d9404e86
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243357951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26dc391261be743a895f112c161932e5112c32275cb7c47e7d2a9094a0c34ac1`
-	Default Command: `["jshell"]`

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
# Wed, 16 Sep 2020 23:32:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:32:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-15-jdk=15     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:32:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-15
# Wed, 16 Sep 2020 23:32:31 GMT
CMD ["jshell"]
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
	-	`sha256:bd5faa0a96b48ae527730113e24fa29b4ec30f2a3c1f183433b1d9bce93024d2`  
		Last Modified: Wed, 16 Sep 2020 23:33:23 GMT  
		Size: 8.3 MB (8316864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ba2aa1c2be24967cda0e6680a94d396dd0f0fc18e40a8979483aa47e0f8007`  
		Last Modified: Wed, 16 Sep 2020 23:33:45 GMT  
		Size: 206.5 MB (206482920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
