## `hitch:latest`

```console
$ docker pull hitch@sha256:5813eee855d89ac513ccc8074c72b98d787ea4a3637ff3578a9a8ffe3a9ffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:675f9679049b98c6d8df8701c18aa77aea120014d7e11fd8622a9484ed16dd9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca7964fd36a5abb2e31b2d6a59f31acf4b3648a6ca6497d8388cf4f5f461a1d`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Mon, 18 Oct 2021 19:23:04 GMT
ARG SRCVER=1.7.0
# Mon, 18 Oct 2021 19:23:04 GMT
ARG PKGVER=1
# Mon, 18 Oct 2021 19:23:04 GMT
ARG DISTVER=bullseye
# Mon, 18 Oct 2021 19:23:04 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Mon, 18 Oct 2021 19:23:04 GMT
ARG SHASUM=d82d2cb5d0be39dcd40ffd969d0a1c25d4d253c21078f8b2b1fca7a4e93acc84c15a53590966917b6382faffc24abdc7928b713460b1f28a321ac5b8fafd8313
# Mon, 18 Oct 2021 19:24:57 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=d82d2cb5d0be39dcd40ffd969d0a1c25d4d253c21078f8b2b1fca7a4e93acc84c15a53590966917b6382faffc24abdc7928b713460b1f28a321ac5b8fafd8313 SRCVER=1.7.0
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Mon, 18 Oct 2021 19:24:57 GMT
WORKDIR /etc/hitch
# Mon, 18 Oct 2021 19:24:57 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Mon, 18 Oct 2021 19:24:58 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Mon, 18 Oct 2021 19:24:58 GMT
EXPOSE 443
# Mon, 18 Oct 2021 19:24:58 GMT
CMD []
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8060cae2ab03f76c57506befb196263e056eaab8f2fba549f2d69cb942c8f392`  
		Last Modified: Mon, 18 Oct 2021 19:25:21 GMT  
		Size: 1.6 MB (1623264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db2a5adee5144934005b23b4a59df44c9e12799d3c1b1e094999759a8c504ad`  
		Last Modified: Mon, 18 Oct 2021 19:25:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
