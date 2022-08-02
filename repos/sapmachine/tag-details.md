<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.16`](#sapmachine11016)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.4`](#sapmachine1704)
-	[`sapmachine:18`](#sapmachine18)
-	[`sapmachine:18.0.2`](#sapmachine1802)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:1bd38649b1175383db9a7df57c27e038205d92c440fb2e81628030c65a667575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:b7974b62912c4c5e7709aca41bf3ff7303894eefd639062315602a03eebf8b70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234327294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12b9ffbcebfa18b2e4eb4157214e574cd2f261b01e7aa9d40924f638d7db831`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:50:48 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:50:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 02 Aug 2022 20:50:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883230c0f6895d0e45586c444fd9de9d51c84363a3abd4fcef20977463bc1278`  
		Last Modified: Tue, 02 Aug 2022 20:52:33 GMT  
		Size: 197.8 MB (197834456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.16`

```console
$ docker pull sapmachine@sha256:1bd38649b1175383db9a7df57c27e038205d92c440fb2e81628030c65a667575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.16` - linux; amd64

```console
$ docker pull sapmachine@sha256:b7974b62912c4c5e7709aca41bf3ff7303894eefd639062315602a03eebf8b70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234327294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12b9ffbcebfa18b2e4eb4157214e574cd2f261b01e7aa9d40924f638d7db831`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:50:48 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:50:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 02 Aug 2022 20:50:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883230c0f6895d0e45586c444fd9de9d51c84363a3abd4fcef20977463bc1278`  
		Last Modified: Tue, 02 Aug 2022 20:52:33 GMT  
		Size: 197.8 MB (197834456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:acd45e7e8a26f4afd2e94c9142126db54f08e76999e9575bc894b7759b059da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:3be101e12c4ecf8c7c46dba53b7c5d833b2c498c7dcd11e567efa68f841600f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233708749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33453c5dc3e151a9ac963fe35f3c7ec927280510cb737c6f78d6e27ccc283760`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Aug 2022 20:51:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e450e1d764f78da00304a3a4f962c25a214c558e12c2d836a422644944e0d1`  
		Last Modified: Tue, 02 Aug 2022 20:52:59 GMT  
		Size: 197.2 MB (197215911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.4`

```console
$ docker pull sapmachine@sha256:acd45e7e8a26f4afd2e94c9142126db54f08e76999e9575bc894b7759b059da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.4` - linux; amd64

```console
$ docker pull sapmachine@sha256:3be101e12c4ecf8c7c46dba53b7c5d833b2c498c7dcd11e567efa68f841600f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233708749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33453c5dc3e151a9ac963fe35f3c7ec927280510cb737c6f78d6e27ccc283760`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Aug 2022 20:51:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e450e1d764f78da00304a3a4f962c25a214c558e12c2d836a422644944e0d1`  
		Last Modified: Tue, 02 Aug 2022 20:52:59 GMT  
		Size: 197.2 MB (197215911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18`

```console
$ docker pull sapmachine@sha256:4e07118cb553ebf333868979b742dc64e5939e936e10b249e249528a8cf09ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18` - linux; amd64

```console
$ docker pull sapmachine@sha256:3432e651575e0a007bd603dfe1c8e626a3f53485d63fac6802fdeaec39187b5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234756159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60948288ac9ed39c9d3260649f8dfbef94df34ce3ba83c3f2daa372ea0d62262`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:52:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:52:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Tue, 02 Aug 2022 20:52:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d6892687f79c0d44f7afbc9a68f8d2d2d4d3b112a6038bfd55695f8cb498a9`  
		Last Modified: Tue, 02 Aug 2022 20:53:27 GMT  
		Size: 198.3 MB (198263321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18.0.2`

```console
$ docker pull sapmachine@sha256:4e07118cb553ebf333868979b742dc64e5939e936e10b249e249528a8cf09ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18.0.2` - linux; amd64

```console
$ docker pull sapmachine@sha256:3432e651575e0a007bd603dfe1c8e626a3f53485d63fac6802fdeaec39187b5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234756159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60948288ac9ed39c9d3260649f8dfbef94df34ce3ba83c3f2daa372ea0d62262`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:52:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:52:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Tue, 02 Aug 2022 20:52:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d6892687f79c0d44f7afbc9a68f8d2d2d4d3b112a6038bfd55695f8cb498a9`  
		Last Modified: Tue, 02 Aug 2022 20:53:27 GMT  
		Size: 198.3 MB (198263321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:4e07118cb553ebf333868979b742dc64e5939e936e10b249e249528a8cf09ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:3432e651575e0a007bd603dfe1c8e626a3f53485d63fac6802fdeaec39187b5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234756159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60948288ac9ed39c9d3260649f8dfbef94df34ce3ba83c3f2daa372ea0d62262`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:52:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:52:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Tue, 02 Aug 2022 20:52:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d6892687f79c0d44f7afbc9a68f8d2d2d4d3b112a6038bfd55695f8cb498a9`  
		Last Modified: Tue, 02 Aug 2022 20:53:27 GMT  
		Size: 198.3 MB (198263321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:acd45e7e8a26f4afd2e94c9142126db54f08e76999e9575bc894b7759b059da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:3be101e12c4ecf8c7c46dba53b7c5d833b2c498c7dcd11e567efa68f841600f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233708749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33453c5dc3e151a9ac963fe35f3c7ec927280510cb737c6f78d6e27ccc283760`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Aug 2022 20:51:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e450e1d764f78da00304a3a4f962c25a214c558e12c2d836a422644944e0d1`  
		Last Modified: Tue, 02 Aug 2022 20:52:59 GMT  
		Size: 197.2 MB (197215911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
