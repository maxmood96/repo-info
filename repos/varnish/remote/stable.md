## `varnish:stable`

```console
$ docker pull varnish@sha256:e0268f7517a2376eb0cf44349283c5cdb654de178e8106da3c25df01337dc9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:e4cd2e7566f7b0bb6024b2bbc7afbcc0051578eda02a26f23e6eb0f2fb1d8b17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100654177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3021a46bbb249a168c045b9b28ed52b3080066ecd5c56949a13f602a883fe5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 06:45:19 GMT
ENV VARNISH_SIZE=100M
# Thu, 09 Feb 2023 06:47:30 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 09 Feb 2023 06:47:31 GMT
WORKDIR /etc/varnish
# Thu, 09 Feb 2023 06:47:31 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 09 Feb 2023 06:47:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 09 Feb 2023 06:47:31 GMT
EXPOSE 80 8443
# Thu, 09 Feb 2023 06:47:31 GMT
CMD []
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80050f63f771eb4efeb5c0520d8f026ffeb09052cc3d2e9ad6a21a0b9e421d9`  
		Last Modified: Thu, 09 Feb 2023 06:48:55 GMT  
		Size: 69.2 MB (69241665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6274344d07d3f36b703541c8cbd5a4af391685ca105a99b7428780321587d14`  
		Last Modified: Thu, 09 Feb 2023 06:48:46 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm variant v7

```console
$ docker pull varnish@sha256:b12e1f3fa3543f6b62c6936050c5c49e395526b6bbd513d564cc20c3400da14b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77228790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eaa8234f17aafa0a6d1f10a6c8c569b2d73071f16693a509571a15ff1490f0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 09 Feb 2023 06:12:09 GMT
ADD file:5f1a343224e8486690bd90dd1e50c8d84b3d770c51bb6829544e5cf650c0419c in / 
# Thu, 09 Feb 2023 06:12:10 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:07:34 GMT
ENV VARNISH_SIZE=100M
# Thu, 09 Feb 2023 13:09:47 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 09 Feb 2023 13:09:47 GMT
WORKDIR /etc/varnish
# Thu, 09 Feb 2023 13:09:48 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 09 Feb 2023 13:09:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 09 Feb 2023 13:09:48 GMT
EXPOSE 80 8443
# Thu, 09 Feb 2023 13:09:48 GMT
CMD []
```

-	Layers:
	-	`sha256:e7318f6106ad75d7d482ae9dddf4d927b0872ef3ddb6e1330aa691fc8d17279e`  
		Last Modified: Thu, 09 Feb 2023 06:19:19 GMT  
		Size: 26.6 MB (26577666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4b0e138e40efd679262e2d1b7f8fb6756f6503f5c923a61f59f70fd06b3bf2`  
		Last Modified: Thu, 09 Feb 2023 13:12:00 GMT  
		Size: 50.7 MB (50650423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dff13124e90d8714fff8b78a63bb272388d8aacba46a4c07b3971b1b7171f0`  
		Last Modified: Thu, 09 Feb 2023 13:11:51 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:c450ad79500ba96cc35dd3c52ad3599334e6b3041428c499f6be27e07f1d22c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94715178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcf86c429658bbe854449e54a0595d02f2cd4d0cd0a866950b73caa3b511092`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 08:49:30 GMT
ENV VARNISH_SIZE=100M
# Thu, 09 Feb 2023 08:51:12 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 09 Feb 2023 08:51:12 GMT
WORKDIR /etc/varnish
# Thu, 09 Feb 2023 08:51:12 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 09 Feb 2023 08:51:12 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 09 Feb 2023 08:51:12 GMT
EXPOSE 80 8443
# Thu, 09 Feb 2023 08:51:12 GMT
CMD []
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf53fb8b108e21aca2703892f32fa2f2619b742b46646331e3de24ab29d2ff0`  
		Last Modified: Thu, 09 Feb 2023 08:52:40 GMT  
		Size: 64.7 MB (64651966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221a70689e8a24c44e0e2d2a614e95e20e58ad7b87f01b72f52870e353b77c63`  
		Last Modified: Thu, 09 Feb 2023 08:52:33 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; 386

```console
$ docker pull varnish@sha256:f56aa456fae0b77ca66bec4fe85700f8781a3884de98883c8ff959c9dd055f2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102061249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de466f497ac50aeb90f89b48ee5a85c34f954ccb439cd58cafdc8cb74267e295`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 04 Feb 2023 07:49:22 GMT
ADD file:82af884aad6a87f5b309a7418aa1df69f92180a39818ae6d77d37d072cb6fecb in / 
# Sat, 04 Feb 2023 07:49:22 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 21:42:34 GMT
ENV VARNISH_SIZE=100M
# Sat, 04 Feb 2023 21:45:00 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Sat, 04 Feb 2023 21:45:00 GMT
WORKDIR /etc/varnish
# Sat, 04 Feb 2023 21:45:02 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Sat, 04 Feb 2023 21:45:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Sat, 04 Feb 2023 21:45:03 GMT
EXPOSE 80 8443
# Sat, 04 Feb 2023 21:45:04 GMT
CMD []
```

-	Layers:
	-	`sha256:fb99e0a97d653ef9acb2bdac0d1d10a8655b789bd4e8924c4a1c4a2af8adbb4a`  
		Last Modified: Sat, 04 Feb 2023 07:55:04 GMT  
		Size: 32.4 MB (32375772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2e84e91a218f50a680c6e76813b7dc715f8531d7019f32602ffd231bc68c52`  
		Last Modified: Sat, 04 Feb 2023 21:46:29 GMT  
		Size: 69.7 MB (69684776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caa57957b3cf341e896f98722d6ad32929b1ea6ddd1a3934ed40cdd62d247eb`  
		Last Modified: Sat, 04 Feb 2023 21:46:20 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; ppc64le

```console
$ docker pull varnish@sha256:193cbaeb322e0557f034c425514d885339d6668c4386aa513402721bd9c21133
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99799855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda082de4c7749b8307345a3b8d4137b5dabdedcabcd421708578b85a9e9a489`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:04:27 GMT
ENV VARNISH_SIZE=100M
# Thu, 09 Feb 2023 12:11:06 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 09 Feb 2023 12:11:08 GMT
WORKDIR /etc/varnish
# Thu, 09 Feb 2023 12:11:09 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 09 Feb 2023 12:11:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 09 Feb 2023 12:11:10 GMT
EXPOSE 80 8443
# Thu, 09 Feb 2023 12:11:10 GMT
CMD []
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d53de417bdc50d62d7fdbeeea8e46800fabd0ed80370a9069c87147b7123ad5`  
		Last Modified: Thu, 09 Feb 2023 12:13:28 GMT  
		Size: 64.5 MB (64509900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622e78faebf5b8024d64bf97cbc1e0a1a2ef6e8ed2fddbb16abfc817471fc463`  
		Last Modified: Thu, 09 Feb 2023 12:13:11 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `varnish:stable` - linux; s390x

```console
$ docker pull varnish@sha256:df592d2c04da7cb2ee2144d4d971e719e7a60555c989bb86dde0d6c56089a79f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81002185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73636281614290efddc6e2f074b73a8ae88c72ab5f8d5e59d9349b2e0b0203b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 04:36:52 GMT
ENV VARNISH_SIZE=100M
# Thu, 09 Feb 2023 04:41:52 GMT
RUN set -e;     BASE_PKGS="curl dpkg-dev debhelper devscripts equivs git pkg-config apt-utils fakeroot";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;     tmpdir="$(mktemp -d)";     cd "$tmpdir";     apt-get update;     apt-get install -y $BASE_PKGS;     git clone https://github.com/varnishcache/pkg-varnish-cache.git;     cd pkg-varnish-cache;     git checkout 10da6a585eb7d8defe9d273a51df5b133500eb6b;     rm -rf .git;     curl -f https://varnish-cache.org/downloads/varnish-6.0.11.tgz -o $tmpdir/orig.tgz;     echo "02f56f360c6bbed663e712edef961384e6003cfe73307c7ea50f805ac4b4df0d26958179170401a2254a69ab623acc172da42926d82189bfa724a4e8a78597ea  $tmpdir/orig.tgz" | sha512sum -c -;     tar xavf $tmpdir/orig.tgz --strip 1;     sed -i -e "s|@VERSION@|6.0.11|"  "debian/changelog";     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --yes" debian/control;     sed -i '' debian/varnish*;     dpkg-buildpackage -us -uc -j"$(nproc)";     apt-get -y install ../*.deb;     apt-get -y purge --auto-remove varnish-build-deps $BASE_PKGS;     mkdir /pkgs;     mv ../*dev*.deb /pkgs;     rm -rf /var/lib/apt/lists/* "$tmpdir";
# Thu, 09 Feb 2023 04:42:02 GMT
WORKDIR /etc/varnish
# Thu, 09 Feb 2023 04:42:02 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 09 Feb 2023 04:42:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 09 Feb 2023 04:42:03 GMT
EXPOSE 80 8443
# Thu, 09 Feb 2023 04:42:04 GMT
CMD []
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745410423134e2a363bf94f19d54352747cc0d7d642545ec7a337ad28c334724`  
		Last Modified: Thu, 09 Feb 2023 04:43:20 GMT  
		Size: 51.4 MB (51353971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e967e8ebb718a1ca31b86298d62b3fdfdcf3fac94d321d34ba0754a9c55395`  
		Last Modified: Thu, 09 Feb 2023 04:43:14 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
