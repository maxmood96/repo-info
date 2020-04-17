## `swift:latest`

```console
$ docker pull swift@sha256:dce58d0c86186172c94166acf004d3cad169e03a03a43ada5c25486fe702d63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:b87ba67d39ff1900590091df251063ccdf3567512feae7d68b086c584c312d59
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **536.3 MB (536267268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b82ca557c3cb03599e94bd65fed7cddbcabb3f264c7ca4e8d1ac95d480fca8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:39:51 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 20 Mar 2020 20:39:51 GMT
LABEL Description=Docker Container for the Swift programming language
# Fri, 20 Mar 2020 20:40:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libatomic1     libcurl4     libxml2     libedit2     libsqlite3-0     libc6-dev     binutils     libgcc-5-dev     libstdc++-5-dev     zlib1g-dev     libpython2.7     tzdata     git     pkg-config     && rm -r /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:40:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 20 Mar 2020 20:40:32 GMT
ARG SWIFT_PLATFORM=ubuntu18.04
# Fri, 17 Apr 2020 20:28:46 GMT
ARG SWIFT_BRANCH=swift-5.2.2-release
# Fri, 17 Apr 2020 20:28:46 GMT
ARG SWIFT_VERSION=swift-5.2.2-RELEASE
# Fri, 17 Apr 2020 20:28:46 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 17 Apr 2020 20:28:47 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu18.04 SWIFT_BRANCH=swift-5.2.2-release SWIFT_VERSION=swift-5.2.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 17 Apr 2020 20:30:18 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 17 Apr 2020 20:30:20 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31697690bbc450a03e1ee66b383f27cd927b6ea1278038c3cb6d97d530254068`  
		Last Modified: Fri, 20 Mar 2020 20:47:15 GMT  
		Size: 124.1 MB (124128545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4374ec7c5291b5900f56b37b8345f61fc10913dc156b04fd8ed43f132b4b055d`  
		Last Modified: Fri, 17 Apr 2020 20:37:03 GMT  
		Size: 385.4 MB (385411754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
