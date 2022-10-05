## `hitch:latest`

```console
$ docker pull hitch@sha256:b467b331f5520d24e0346f182b3a40a6145cce930532960b315e56119cc18b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hitch:latest` - linux; amd64

```console
$ docker pull hitch@sha256:1dc528ee8ded0bdf462770d1339bb917ce2d142a144611722d910061d5e94cec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33029828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42336b34c513f995233303991cd2e4d474409dbcd7ef2c7547d571e4de734c73`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 17:19:58 GMT
ARG SRCVER=1.7.3
# Wed, 14 Sep 2022 17:19:58 GMT
ARG PKGVER=1
# Wed, 14 Sep 2022 17:19:58 GMT
ARG DISTVER=bullseye
# Wed, 14 Sep 2022 17:19:59 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 14 Sep 2022 17:19:59 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 14 Sep 2022 17:21:50 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 14 Sep 2022 17:21:51 GMT
WORKDIR /etc/hitch
# Wed, 14 Sep 2022 17:21:51 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 14 Sep 2022 17:21:51 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 14 Sep 2022 17:21:51 GMT
EXPOSE 443
# Wed, 14 Sep 2022 17:21:51 GMT
CMD []
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceda6c4b73d1d43588a606af96b153a07ea72cdb6406c72d4d46f107d98cbfea`  
		Last Modified: Wed, 14 Sep 2022 17:22:16 GMT  
		Size: 1.6 MB (1625289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f430fe2884114d14113ebed16d701f38328c0a144174005970cdc35f706e5bde`  
		Last Modified: Wed, 14 Sep 2022 17:22:15 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm variant v7

```console
$ docker pull hitch@sha256:02606a211f1ad566f3d8b45eeb5858f39f64d0b5b4ae0a671ac7114eb7133fc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28112089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f547947a7ff7c84643de18ccb1bb442a27432dec40bcc88962ee5fc9aaf18220`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Thu, 15 Sep 2022 03:13:28 GMT
ARG SRCVER=1.7.3
# Thu, 15 Sep 2022 03:13:28 GMT
ARG PKGVER=1
# Thu, 15 Sep 2022 03:13:28 GMT
ARG DISTVER=bullseye
# Thu, 15 Sep 2022 03:13:28 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Thu, 15 Sep 2022 03:13:28 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Thu, 15 Sep 2022 03:15:33 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Thu, 15 Sep 2022 03:15:33 GMT
WORKDIR /etc/hitch
# Thu, 15 Sep 2022 03:15:33 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Thu, 15 Sep 2022 03:15:33 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Thu, 15 Sep 2022 03:15:33 GMT
EXPOSE 443
# Thu, 15 Sep 2022 03:15:33 GMT
CMD []
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4fdcbd642a367c2414d715be53717329c86538c61ea8c8366d8c630d486408`  
		Last Modified: Thu, 15 Sep 2022 03:16:04 GMT  
		Size: 1.5 MB (1544612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b84e681893afee3bf8ab0b7a0708f5c84b35cfce5af2d842b60ef642d042c8`  
		Last Modified: Thu, 15 Sep 2022 03:16:04 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; arm64 variant v8

```console
$ docker pull hitch@sha256:480caa4826ab55b18680872b84b81a3cd8a5b353b78097aed02447566278e5d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31660004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afbfdfd18ead3c49b74d26c78c69ae7db952ceabb7c6df46473395a384b73c0`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 17:39:49 GMT
ARG SRCVER=1.7.3
# Wed, 14 Sep 2022 17:39:49 GMT
ARG PKGVER=1
# Wed, 14 Sep 2022 17:39:50 GMT
ARG DISTVER=bullseye
# Wed, 14 Sep 2022 17:39:51 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 14 Sep 2022 17:39:52 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 14 Sep 2022 17:41:35 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 14 Sep 2022 17:41:36 GMT
WORKDIR /etc/hitch
# Wed, 14 Sep 2022 17:41:38 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 14 Sep 2022 17:41:38 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 14 Sep 2022 17:41:39 GMT
EXPOSE 443
# Wed, 14 Sep 2022 17:41:40 GMT
CMD []
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f4826655b58aa4a89d9e0092954bb02c1edf7750177bd4c0c85cb7216b43f7`  
		Last Modified: Wed, 14 Sep 2022 17:41:59 GMT  
		Size: 1.6 MB (1605347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e0f175f732610c1f7561a24db711b993dbe90c08dfe71373f5bf864f7ea9c1`  
		Last Modified: Wed, 14 Sep 2022 17:41:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; 386

```console
$ docker pull hitch@sha256:cdd479b1dec185b6f74cd73c52dd9551ee4da9ce1082eae37b88749f5764ec2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34013029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86438e38621bf946d16480f7e956506842bb9c6caf3d0e0e00cfd42a5add582`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 17:38:34 GMT
ARG SRCVER=1.7.3
# Wed, 14 Sep 2022 17:38:35 GMT
ARG PKGVER=1
# Wed, 14 Sep 2022 17:38:36 GMT
ARG DISTVER=bullseye
# Wed, 14 Sep 2022 17:38:37 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 14 Sep 2022 17:38:38 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 14 Sep 2022 17:40:26 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 14 Sep 2022 17:40:27 GMT
WORKDIR /etc/hitch
# Wed, 14 Sep 2022 17:40:29 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 14 Sep 2022 17:40:29 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 14 Sep 2022 17:40:30 GMT
EXPOSE 443
# Wed, 14 Sep 2022 17:40:31 GMT
CMD []
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48404c45c6c8fe96eea083bf1c678573ef43cfb5511036d59355dddd76a0e7d4`  
		Last Modified: Wed, 14 Sep 2022 17:40:59 GMT  
		Size: 1.6 MB (1628823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2102cf9c0d53d71ebad1a7f9d7615ebc075df89e5a0496479dfa69ee221d0b7`  
		Last Modified: Wed, 14 Sep 2022 17:40:58 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; ppc64le

```console
$ docker pull hitch@sha256:aef9636130baad766a8865bc0a547fd3c13f77664af349f6577e46383cc50592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36976726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448f5a3e0ba9222fc71277bdee6606e5ce99bf011717c171edc17484b5941c05`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Oct 2022 23:18:04 GMT
ADD file:66a0f55a4b4dfbb5d64082ffdb24751f20c5773039277ba278fdb4ce4a538c33 in / 
# Tue, 04 Oct 2022 23:18:06 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:00:29 GMT
ARG SRCVER=1.7.3
# Wed, 05 Oct 2022 01:00:30 GMT
ARG PKGVER=1
# Wed, 05 Oct 2022 01:00:30 GMT
ARG DISTVER=bullseye
# Wed, 05 Oct 2022 01:00:30 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 05 Oct 2022 01:00:30 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 05 Oct 2022 01:05:00 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 05 Oct 2022 01:05:01 GMT
WORKDIR /etc/hitch
# Wed, 05 Oct 2022 01:05:01 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 05 Oct 2022 01:05:02 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 05 Oct 2022 01:05:02 GMT
EXPOSE 443
# Wed, 05 Oct 2022 01:05:03 GMT
CMD []
```

-	Layers:
	-	`sha256:4e001127162dd884a6f7bd2e6f74215816d325bebb3a374ae9fcee9f038f99b8`  
		Last Modified: Tue, 04 Oct 2022 23:24:13 GMT  
		Size: 35.3 MB (35290584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c47ce2d6eb834e6aea14721c3590d86bbad7a77c833d00eba6f03cee5705c17`  
		Last Modified: Wed, 05 Oct 2022 01:09:40 GMT  
		Size: 1.7 MB (1685725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3acccc09b92b264d693c7278e015a528cbce29e6f53f9fcd8841507b95ae15e`  
		Last Modified: Wed, 05 Oct 2022 01:09:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hitch:latest` - linux; s390x

```console
$ docker pull hitch@sha256:34847678fc7db4e29cb9d71c7c3bee791a529923d2c2b2af901da500a13aac27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31272868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca021ac184cde0e809a5ea16eb5b2f13621080e0ba4d15a72c13112c525ca525`
-	Entrypoint: `["docker-hitch-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 04 Oct 2022 23:42:42 GMT
ADD file:7acfe92be51da9cffeb5b063cc87926d1ce457729e3080de340603a38216a708 in / 
# Tue, 04 Oct 2022 23:42:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:11:26 GMT
ARG SRCVER=1.7.3
# Wed, 05 Oct 2022 01:11:26 GMT
ARG PKGVER=1
# Wed, 05 Oct 2022 01:11:26 GMT
ARG DISTVER=bullseye
# Wed, 05 Oct 2022 01:11:26 GMT
ARG PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794
# Wed, 05 Oct 2022 01:11:26 GMT
ARG SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd
# Wed, 05 Oct 2022 01:13:16 GMT
# ARGS: DISTVER=bullseye PKGCOMMIT=f12ab7958bc4885f3f00311cbca5103d9e6ba794 PKGVER=1 SHASUM=88de82e639e7f9b7873bb7226fcbcbc4cd5779c75a5bd21fca8e1ca927a2a3ae9eb455d73d1f42d4dc45546118c718d1b58396836ed9c8acac281d487c9fe8fd SRCVER=1.7.3
RUN set -ex;     BASE_PKGS="apt-utils curl dirmngr dpkg-dev debhelper devscripts equivs fakeroot git gnupg pkg-config";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnish/pkg-hitch.git;     cd pkg-hitch;     git checkout ${PKGCOMMIT};     rm -rf .git;     curl -Lf https://hitch-tls.org/source/hitch-${SRCVER}.tar.gz -o $tmpdir/orig.tgz;     echo "${SHASUM}  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i         -e "s/@SRCVER@/${SRCVER}/g"         -e "s/@PKGVER@/${PKGVER:-1}/g"         -e "s/@DISTVER@/$DISTVER/g" debian/changelog;     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/hitch*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y purge --auto-remove hitch-build-deps $BASE_PKGS;     apt-get -y install ../*.deb;     sed -i 's/daemon = on/daemon = off/' /etc/hitch/hitch.conf;     rm -rf /var/lib/apt/lists/* "$tmpdir"
# Wed, 05 Oct 2022 01:13:16 GMT
WORKDIR /etc/hitch
# Wed, 05 Oct 2022 01:13:16 GMT
COPY file:1abf3c94dce5dc9f6617dc8d36a6fe6f4f7236189d4819f16cefb54288e80e0d in /usr/local/bin/ 
# Wed, 05 Oct 2022 01:13:16 GMT
ENTRYPOINT ["docker-hitch-entrypoint"]
# Wed, 05 Oct 2022 01:13:17 GMT
EXPOSE 443
# Wed, 05 Oct 2022 01:13:17 GMT
CMD []
```

-	Layers:
	-	`sha256:62990b94a520bfcf718ec711f8444f83c536af2c83c8e53fdfe1f89fdcb79826`  
		Last Modified: Tue, 04 Oct 2022 23:47:16 GMT  
		Size: 29.7 MB (29650719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17afc180f02764cf61833ae606cadcdecbd185b87ce84699db8ae5b73dfa2b8c`  
		Last Modified: Wed, 05 Oct 2022 01:16:12 GMT  
		Size: 1.6 MB (1621733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4937b0482ead9a2ceea3a620c90fa16d7b0ea3122d256d72945ac78f8c53fb7c`  
		Last Modified: Wed, 05 Oct 2022 01:16:12 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
